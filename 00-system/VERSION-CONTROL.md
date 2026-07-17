---
document_type: version-control-policy
status: active
last_updated: 2026-07-17
---

# Version Control Policy

## Repository Model

Use two separate public GitHub repositories:

1. Source repository for fpcXUI source code, tests, and repository-local development files
2. Memory repository for the portable Obsidian Markdown knowledge system

| Repository | GitHub | SSH remote | Visibility |
| --- | --- | --- | --- |
| fpcXUI source | [jedt3d/fpcXUI](https://github.com/jedt3d/fpcXUI) | `git@github.com:jedt3d/fpcXUI.git` | Public |
| fpcXUI memory | [jedt3d/fpcXUI-memory](https://github.com/jedt3d/fpcXUI-memory) | `git@github.com:jedt3d/fpcXUI-memory.git` | Public |

Both repositories had an initial MIT `LICENSE` commit on `main` when verified on 2026-07-17. The user authorized replacing those remote branches with the current local snapshots while preserving the same MIT `LICENSE` in each repository root. This is a one-time publication authorization and does not define future commit or push authority.

## Memory Working Location

- Keep the active Obsidian vault at its selected OneDrive location.
- Treat the memory repository and the Obsidian vault as the same working tree after Git is initialized there.
- OneDrive provides file synchronization; GitHub provides reviewed, versioned history and agent sharing.

## Single-Computer Write Rule

1. Only one computer may modify or commit the vault at a time.
2. Before changing memory on another computer, finish and synchronize work from the current computer.
3. Confirm the Git working tree and remote state before beginning a new memory-writing session.
4. Do not edit the vault concurrently on multiple computers.
5. If OneDrive or Git presents conflicting versions, stop and inspect both versions before resolving the conflict.

## Cross-Repository References

- Source-code evidence in memory documents should identify the source repository and a portable file path.
- Handoffs should identify the relevant repository, branch, and commit when available.
- Do not use machine-specific absolute paths as permanent cross-repository references.

## Exclusion and Security Rules

- The memory repository is public; review the complete staged change before every commit and push.
- Do not commit Obsidian workspace state.
- Do not commit agent sessions or agent-private configuration.
- Do not commit plugin binaries or plugin-private data.
- Do not commit credentials, API keys, access tokens, private keys, or environment-secret files.
- Treat `.gitignore` as a safety layer, not as permission to store secrets in the vault.

## Pending Decisions

- Whether Codex may create commits automatically after validated memory updates
- Whether Codex may push only with explicit user approval
