# community-plugins — Changelog

Date format: `YYYY-MM-DD`. One section per run/campaign. Append newest at the top.
Each run records what happened and the verification evidence tied to its exact
commit range, so we always know the state we resume from.

---

## 2026-08-22 — Initial repo scaffold

**Driver / controller:** FRIDAY (default profile)
**Branch:** main
**Commit range:** (initial commit)
**Head SHA:** see `git rev-parse HEAD`
**Scope (approved):** Create public curated-list repo for community desktop plugins. Description + link rows only; no code hosting, no auto-publish.
**What changed (non-exhaustive):**
- README.md: layperson-first intro to desktop plugins, install steps, table format, submission requirements
- PULL_REQUEST_TEMPLATE.md: submission checklist
- .github/ISSUE_TEMPLATE/plugin-listing.md: fallback issue form for non-PR submitters
- LICENSE: MIT with third-party listing disclaimer
- Starter row: hermes-tool-router as the example entry
**Verification:** Files written and verified on disk; repo created via `gh repo create` (public); pushed to origin/main.
**Status:** CODE-COMPLETE
**Next-run resume point:** Update org front-page README (AtlasOmnia/AtlasOmnia) Community section to link this repo; optionally pin the repo; add monthly link-liveness check if approved.

---

<!-- Template for future entries — duplicate the YYYY-MM-DD block above when a
new run starts, and keep it at the top of the section history. -->
