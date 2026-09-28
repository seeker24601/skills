---
name: dissolve-page
description: Redistribute a page into canonical destinations, preserve evidence, and repair references before retiring its content.
version: 0.1.0
classes: ARCHIVIST
metadata:
  hermes:
    tags: [archive, records, knowledge, maintenance]
    category: productivity
---

# Dissolve Page

Use for a requested split, merge, consolidation, or retirement of a synthesized page. Follow `AGENTS.md` for scope, preservation, and vault tool use.

1. Resolve and read the exact source, local filing rules, parent index, and potential destinations. Retain its original content for comparison. Do not dissolve raw evidence, generated or protected pages, append-only history, indexes, or canonical roots. If ownership or edit authority is unclear, resolve that choice before changing records.
2. Inventory every distinct claim, definition, event, decision, source, uncertainty, and outbound link. Search incoming links using the path, title, stem, and aliases; note any search limits.
3. Read candidate owners rather than selecting by title. Map each content unit to an existing destination or a justified new subject page. Drop only exact duplicates or explicitly authorized content; preserve provenance beside each claim and keep conflicting accounts visible.
4. Integrate units into destinations using their existing structure. Preserve dates, confidence, reasons, and counterevidence. Write with fresh hashes and read back before altering the source. If any save fails, keep the original source intact and report partial progress.
5. Repair incoming links to the destination owning the referenced subject. Update appropriate indexes and meaningful relationships. Build replacement access routes for pages whose only incoming link was the source. Do not add generic links merely to make a graph dense.
6. Compare destinations against the original inventory. Every unique unit and source must be accounted for; validate affected links and search for stale references. Reconcile concurrent changes before continuing.
7. Only after preservation checks pass, replace the source body with a brief retirement pointer naming the destination pages and their subjects. Preserve metadata or history required by local rules. If checks or coverage are incomplete, leave the source intact.

The bundled vault tool has no delete or rename operation. Do not bypass it with shell commands or claim actual deletion. Report the retained pointer and any requested deletion as pending an authorized capability. Report destinations, unresolved units, repaired references, and verification limits.
