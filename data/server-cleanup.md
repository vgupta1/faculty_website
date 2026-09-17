# Live-server cleanup list (SFTP)

Two different questions, often confused:

1. **What must never appear on the NEW site.** Handled in the data: the
   19 retired paper PDFs are recorded in `retired_local_pdf` in
   `papers.yml` and are simply not carried forward, and
   `CV_Mar2020_Internal.pdf` is gitignored. Nothing to do.
2. **What should be removed from the OLD server.** Needs Vishal's SFTP;
   the Cowork VM can't reach it. That's the list below.

Decision on file history: Vishal is fine with these files remaining in
the archive repo's git history. No history rewrite. The goal is only
that they are absent from the new site.

Paths are relative to the site root serving
`faculty.marshall.usc.edu/Vishal-Gupta/`.

---

## A. Delete now — privacy

    Papers/CV_Mar2020_Internal.pdf

Publicly downloadable, linked from no page. Also in the archive repo's
pushed history since 7f46b80 — accepted, not being rewritten.

## B. Delete now — superseded duplicates, referenced by nothing

    Papers/DataDriveUSets_OR2.pdf         superseded; live entry uses 10.1007_s10107-017-1125-8.pdf
    Papers/DataDrivenUSets_MProg_v2.pdf   same paper, older draft
    Papers/DataPooling.pdf                superseded by DataPooling_WP.pdf (which IS linked)
    Papers/Debiasing.pdf                  never actually reachable — see note
    Papers/SmallDataTechNote.pdf          superseded by TechNoteSmallData.pdf (which IS linked)
    Papers/syllabus_v1.pdf                unlabeled old syllabus; current ones are linked by name

### Note on Debiasing.pdf

The server has `Debiasing.pdf`. The live `research.html` links
`debiasing.pdf` (lowercase), which does not exist — so that link has
always been a 404 on a case-sensitive server, invisible locally because
macOS is case-insensitive. Nothing has ever successfully downloaded it.

Fixed for the new site by construction: that entry now points at its DOI
and carries no local PDF. `papers.yml` records the capitalized name so
this deletion targets the file that actually exists.

## C. Do NOT delete yet — hold until the new site is live

The 19 paper PDFs whose entries moved to canonical links. They are still
linked by the *current* live `research.html`, so deleting them now breaks
the site that is up today. Authoritative list: `retired_local_pdf` in
`data/papers.yml`. Delete in Session 10, after the new site serves.

## D. Keep permanently

- `Papers/CV.pdf` — linked from nine pages, indexed by Google
- The three papers with no external home, verified present under these
  exact names: `TechNoteSmallData.pdf`,
  `AI_for_Social_Good_Chapter.pdf`, `2021_Gupta_smalldata.pdf`
- All teaching material: syllabi, cases and case questions (ChowHound,
  TrojanHorse, Election, Artsy, DashboardingAtApplichem),
  `all_lectures_singapore.pdf`
- Student project papers linked from `teaching.html`: `chou.pdf`,
  `dylan.pdf`, `spencer.pdf`, `Sanika.pdf`, `dssera.pdf`,
  `SessionPatternPerception.pdf`

## E. Flagged — do not delete, needs a decision

    Papers/mcrary.pdf

Unreferenced, but in the same series as the student project papers above,
all of which ARE linked from `teaching.html`. Likely a student dropped
from the page by accident rather than a duplicate. Resolve in Session 9.

## Build-time guard for the new site

The case bug was silent because macOS hid it. The publications generator
in Session 4 should assert that every `local_pdf` in `papers.yml` exists
on disk with exactly that spelling, and fail the build otherwise. Cheap,
and it catches the whole class of error.
