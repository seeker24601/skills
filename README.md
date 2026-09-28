# Deckr skills

Reusable class instructions, workflows, and skills for Deckr and other agents.

- `classes/<class>/AGENTS.md` defines a class and routes its work.
- `classes/<class>/workflows/` contains task processes.
- `skills/<id>/SKILL.md` contains reusable methods.

Characters select these capabilities separately from their personality and private memory. Archivist methods expect a configured vault tool; Markdown instructions do not install tools or grant access.

## Shared releases

`release.json` identifies a reviewed instruction commit and the SHA-256 hash of each published file. Editing a skill does not publish a release by itself.

After committing instruction changes, run this command from a Deckr source checkout:

```sh
node deckr/distribution/publish-instructions.mjs /path/to/skills
node deckr/distribution/publish-instructions.mjs /path/to/skills --check
```

Review, commit, and push the generated `release.json` to publish that version. The descriptor always points to immutable instruction content.

In the updated Deckr developer client:

```sh
deckr companion sync --dry-run
deckr companion sync
deckr companion sync-status
```

Sync downloads verified instructions and stages them for the next launch. Close Deckr normally, then launch it again. Existing conversations retain their captured class prompts; start a new conversation to use those changes.

Each companion keeps its own editable copies. Local edits and learned changes block updates to that folder and appear in the sync report. Other unchanged companions can update. Personality, memory, vault records, and executable plugins are outside this updater.

A first-time migration adopts existing files only when they exactly match the published release. Later updates compare against the recorded baseline. Use the backup ID from `sync-status` with `deckr companion rollback <backup-id>` to schedule rollback on the next launch. Rollback preserves later edits.

This is an explicit update command. No background polling is enabled. The CLI currently runs from a Deckr source checkout.
