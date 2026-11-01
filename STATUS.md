# STATUS

Project: The Author Visit Handbook
Owner: Asdale Dynamics, LLC
State: complete and verified (November 2026)

## What was built

A beginner-facing manual for local authors arranging friendly, free
author visits, plus the tooling that turns it into an offline static
site. The goal it serves: pitch a library, bookstore, or community
center so staff say yes, plan a fifty-minute session mixing reading,
questions, and a low-key demo of your tools, follow large-print and
plain-English accessibility rules, handle A/V and tables basics, run a
sell-with-dignity book table, thank the host, and turn one visit into
a repeatable kit.

- **docs/** (9 Markdown files: front matter + 7 numbered chapters +
  1 reference page):
  - `00-start-here.md` -- audience, 5-minute quick start,
    conventions, and an explicit "how this differs from the sibling
    handbooks" section.
  1. Pitch the Visit -- venue-by-venue yes factors (library /
     bookstore / community center table), who to contact, the
     8-10-week timing rule, the follow-up ladder, and how to handle
     yes / not-now / no.
  2. Plan the Fifty Minutes -- the minute-by-minute arc table
     (welcome, 8-minute reading, five-minute story, low-key tool
     demo with airplane-mode backup, planted first questions, open
     Q&A with repeated questions, punctual close), plus the
     shorter-slot variant.
  3. Accessibility Without a Committee -- large-print rules (18-point
     projected / 14-point-plus handouts, contrast, line discipline),
     plain-English rules, hearing/eyesight/body-energy habits, and a
     twenty-minute pre-event accessibility pass.
  4. A/V and Tables Basics -- the A/V truce (own laptop, every
     adapter, three save locations, printed fallbacks), the three
     host questions, arrive-30-minutes-early routine, table display
     engineering, and payment basics.
  5. Sell With Dignity -- offer-never-press principles, table setup,
     scripts that keep the selling kind, a banned-lines list, signed
     copies, store-vs-library sales rails, and the ledger/tax note.
  6. Thank the Host -- 48-hour thank-you, public thanks, recap email,
     and the visit-file habit.
  7. Make It Repeatable -- the kit (box + four folders), the one-page
     visit file, living session versions, three-question feedback,
     the season calendar, and the ten-minute pre-visit ritual.
  8. Glossary -- plain-English definitions from "adult programming"
     to "day-of checklist", written to read on the drive over.

- **templates/** (3 Markdown files):
  - `pitch-letter-template.md` -- the one-email pitch with bracketed
    slots, fill-in notes, and a subject-line formula.
  - `day-of-checklist.md` -- printable four-phase checklist (week
    before, thirty minutes before guests, the fifty minutes,
    clean-up) with real ticked checkboxes.
  - `repeatable-kit-inventory.md` -- the printable kit inventory:
    physical box list, four folders, and the one-page visit file.

- **scripts/build.py**: standard-library-only static site generator --
  zero dependencies, zero network. Landing page + 12 content pages
  with sidebar navigation, prev/next pagers, chapter kickers
  ("Chapter 3 of 7"), and an embedded light/dark/print stylesheet in
  a warm terracotta palette. CLI flags: `--out DIR`, `--check` (docs
  lint), `--serve`, `--port`. Pages make no external requests and
  open fine from `file://` or a USB stick.

- **scripts/assets/style.css**: one embedded stylesheet, no external
  requests, dark-mode aware, print-friendly.

- **tests/test_build.py**: 62 tests covering the Markdown converter,
  doc lint, the site builder, the CLI, required-topic coverage (the
  pitch, fifty minutes, accessibility, A/V, selling with dignity,
  thank-yous, repeatable kit), manifest completeness, reproducibility,
  and repo hygiene (secret-pattern scanning, exact LICENSE line,
  README credit, top-level file whitelist).

## How to run it

Requires only Python 3.

```bash
python3 scripts/build.py              # build the site into site/
python3 scripts/build.py --check      # lint the Markdown corpus
python3 scripts/build.py --serve      # build + preview on localhost
python3 -m unittest discover -s tests # run the test suite
```

Open `site/index.html` in any browser afterward.

## Verification results

- `python3 scripts/build.py --check` -- clean (links, anchors,
  titles, placeholders).
- `python3 scripts/build.py` -- built 13 files into site/; build
  checks passed (pages built, links resolve, nothing unresolved).
- `python3 -m unittest discover -s tests` -- 62 tests, all passing:
  build reproducible, repo pages tag-balanced, landing page carries
  the sibling-distinctness note and the Asdale Dynamics, LLC credit,
  no secret patterns, LICENSE contains the exact line
  "Copyright (c) 2026 Asdale Dynamics, LLC", README credits the LLC.
- Landing page repeatedly verified to include
  `author-newsletter-handbook` and `kickstarter-campaign-handbook`
  as the stated non-overlaps.

## Known gaps

- No troubleshooting chapter: if a real-world visit surfaces a
  symptom worth generalizing, it belongs beside the glossary.
- The manual includes no venue-specific posters or flyers; the pitch
  template is the only pre-event artifact. A one-page poster template
  would slot naturally into templates/.
- Language coverage is English-only; a second-language edition would
  need plain-English passages re-verified by a native reviewer.
- The day-of checklist is designed for print but the site does not
  ship a separate print-specific column layout; browsers' built-in
  print scaling is assumed.
