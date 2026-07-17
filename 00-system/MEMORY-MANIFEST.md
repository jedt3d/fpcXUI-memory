---
document_type: memory-manifest
status: active
last_updated: 2026-07-17
---

# Memory Manifest

## System Identity

- Project: fpcXUI
- Memory system: Obsidian vault using portable Markdown
- Vault location: `fpcXUI`
- Repository model: separate public GitHub repositories for source code and memory
- Source repository: [jedt3d/fpcXUI](https://github.com/jedt3d/fpcXUI)
- Source SSH remote: `git@github.com:jedt3d/fpcXUI.git`
- Memory repository: [jedt3d/fpcXUI-memory](https://github.com/jedt3d/fpcXUI-memory)
- Memory SSH remote: `git@github.com:jedt3d/fpcXUI-memory.git`

## Agent Workflow

- Workflow: single AI agent
- Agent: Codex
- Working location: project repository
- Memory permissions: read, create, update, move, and archive, subject to the vault write-access policy below
- Responsibility: inspect project evidence, guide decisions, maintain the authoritative project memory, and verify handoff context

## Authority Rules

1. Codex is the only AI agent participating in the memory workflow.
2. Codex must inspect relevant project evidence before proposing or recording conclusions.
3. Codex must distinguish verified evidence, assumptions, open questions, recommendations, and approved decisions.
4. Codex must follow the guided-autonomy boundaries in [Decision Authority](DECISION-AUTHORITY.md).

## Vault Write-Access Policy

1. Keep the Obsidian vault outside Codex's default writable project workspace.
2. Before changing vault contents, Codex must inspect the permission scope active at that moment.
3. If the active permission scope does not explicitly grant Full Access covering this vault, Codex must request user approval before each memory update.
4. A requested approval may cover one clearly described batch of changes to named memory files.
5. Approval for a memory update does not authorize unrelated changes.
6. If Full Access covering the vault is already active, Codex may perform an otherwise authorized memory update without requesting duplicate approval.

## Version Control

- Follow [Version Control Policy](VERSION-CONTROL.md).
- Permit only one computer at a time to modify and commit the vault.
- Exclude workspace state, agent sessions, credentials, and plugin-private data from Git.
- Treat all trackable memory as publicly visible after push.

## Unresolved Setup Decisions

- Commit and push authority
- Handoff verification protocol
