# Legacy live site snapshot — September 2026

Byte-for-byte copy of what was serving at
http://faculty.marshall.usc.edu/Vishal-Gupta/ before the revamp.

This is the **authoritative record of the old site**, not the Jekyll
source tree in the repo root. They had drifted: this snapshot contains
pages and PDFs that no source file in this repo produces, and newer
versions of several files.

Live-only, with no source anywhere in the repo:
  - apply_page.html                 2024 Summer Scholars program page
  - ResearchActiveFaculty.html      advisor list for PhD applicants
  - CodingLikeAResearcher.html      PhD workshop, Jupyter export (664KB)

Live-only PDFs absent from the repo's own build:
  - Papers/CV_Mar2020_Internal.pdf  (see note below)
  - Papers/DataPooling.pdf
  - Papers/Debiasing.pdf            (repo build had lowercase debiasing.pdf)
  - Papers/syllabus_v1.pdf

Newer live than the repo's build: Papers/CV.pdf,
Papers/3DP_SupplyChainResilience.pdf,
Papers/DecisionAwareDenoising.pdf, research.html

Note: CV_Mar2020_Internal.pdf was publicly reachable on the live server
and linked from no page. Flagged for Vishal; not removed here, since
this folder's job is to record what was live.

Jekyll and Ruby are retired as of this revamp. The root-level
_config.yml, Gemfile, _papers/, _includes/ and _site/ are kept as
history only and are not maintained or built. The new site is
hand-authored HTML in a separate repo.

## Deviation: Ruby dependency files removed

`GemFile` and `Gemfile.lock` were removed from this snapshot (and from the
repo root and `_site/`) after the first push. They are build inputs, not
site content, and Jekyll is retired — nothing installs or runs them.

Keeping them at HEAD made GitHub raise 57 Dependabot vulnerability alerts
against a 2020-era `github-pages` gem bundle (Jekyll 3.4.1/3.8.5, Ruby
2.5.1, nokogiri 1.10.7, kramdown 1.17.0, activesupport 6.0.2.1). None of
those were a real exposure — no CI, no build, nothing installed — but
they generate recurring noise on a repo that is now an archive.

Both files remain in git history if ever needed:
  git show a8971e2:legacy-live-site/Gemfile.lock
