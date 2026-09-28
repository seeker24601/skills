---
name: record-keeping
description: Save useful, sourced Markdown records without losing decisions or uncertainty.
version: 0.2.2
classes: ARCHIVIST
metadata:
  hermes:
    tags: [archive, records, knowledge]
    category: productivity
---

# Record Keeping

Use the vault plugin to search for an existing owner and read it before writing. Prefer updating that page over creating a near-duplicate. Use the existing Home and folder indexes. For an empty vault, create a small `Home.md` entry point and only the folders the records need; do not create a competing README index.

1. Establish what is being recorded, the source, relevant date, and intended destination. Distinguish a decision from a proposal, a quotation from a paraphrase, and an action from an unaccepted suggestion.
2. Write a concise factual note with a descriptive title. Preserve the reasons, constraints, references, unresolved questions, and ownership that make it useful later. Include dates when they affect interpretation. Do not invent missing dates, attendees, agreements, or evidence.
3. Save a new Markdown page, or update the existing page using the plugin's current-content hash protection. If the page changed since you read it, reread and reconcile; never force a stale replacement.
4. Connect the page from its nearest index and include meaningful links to its actual source, project, or related decision where available. Verify the page by reading it back. Do not claim multi-page writes are atomic.
5. Confirm the saved location briefly. If part of the operation fails, say exactly which records exist and which link or index update remains unfinished.

Sensitive persistence follows SOUL.md. Do not automatically copy whole conversations, credentials, or unrelated personal details. Keep revisions and corrections legible instead of silently rewriting a past decision. No external upload is needed for this local archive.

## Note conventions

Use a descriptive filename and one clear H1. When useful, add YAML frontmatter with simple scalar properties such as `type`, `status`, `created`, and `updated`, and inline tags such as `tags: [project, research]`. Use actual ISO dates when known; leave unknown values out. Update `updated` only after a meaningful change. Follow existing conventions rather than reformatting unrelated notes.

Keep Markdown portable. Use `[[Folder/Note|Label]]` for internal links and ordinary Markdown links for external sources. Choose a small number of reusable subject tags. Preserve attribution and distinguish source facts, your synthesis, and open questions in the note itself. The desktop preview supports simple properties and inline tags; avoid relying on an Obsidian-only plugin for essential meaning.

After saving, read `workflows/curate.md` when the record needs inbox triage, index repair, consolidation, or a maintenance pass. Keep this follow-up within the requested scope.
