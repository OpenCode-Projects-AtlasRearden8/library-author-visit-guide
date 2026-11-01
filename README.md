# The Author Visit Handbook

A $0-budget manual for local authors arranging friendly, free visits --
with the pitch that gets the yes, the fifty-minute plan that fills the
hour, and the kit that makes the second visit cost ten minutes. For
the library, the bookstore, or the community center down the road:
book one evening, show up prepared, and be invited back.

Built with warmth, tested locally, and hosted nowhere: this is a
**local-first site**. Run one build command and open `site/index.html`
in your browser -- everything works, forever, offline. No accounts, no
tracking, no affiliate links, no secrets.

> Part of the Asdale Dynamics free tools collection. Written in the
> same spirit as everything else Dylan Asdale makes: explained like a
> friend would, step by step, never condescending.

## What's inside

| File | What it covers |
|---|---|
| [`docs/00-start-here.md`](docs/00-start-here.md) | Front matter: who this is for, a 5-minute quick start, conventions, and how this is distinct from its siblings |
| [`docs/01-pitch-the-visit.md`](docs/01-pitch-the-visit.md) | Chapter 1 -- the pitch that gets library, bookstore, and community-center staff to yes: venue-by-venue yes factors, who to contact, the follow-up ladder |
| [`docs/02-plan-the-fifty-minutes.md`](docs/02-plan-the-fifty-minutes.md) | Chapter 2 -- the fifty-minute session minute by minute: reading, the five-minute story, a low-key demo of your tools, planted questions, and a punctual close |
| [`docs/03-accessibility.md`](docs/03-accessibility.md) | Chapter 3 -- large-print and plain-English rules, hearing and eyesight habits, energy and mobility, and a 20-minute accessibility pass |
| [`docs/04-av-and-tables.md`](docs/04-av-and-tables.md) | Chapter 4 -- the A/V truce (adapters, backups, airplane-mode demo), the three host questions, and table layout that sells |
| [`docs/05-sell-with-dignity.md`](docs/05-sell-with-dignity.md) | Chapter 5 -- the book table for people who buy *and* people who don't: scripts that never press, signed copies, store rails, ledgers |
| [`docs/06-thank-the-host.md`](docs/06-thank-the-host.md) | Chapter 6 -- the 48-hour thank-you, the public thanks, the recap email, and the visit file |
| [`docs/07-make-it-repeatable.md`](docs/07-make-it-repeatable.md) | Chapter 7 -- turning one visit into a repeatable kit: box, four folders, one page per venue, the ten-minute pre-visit ritual |
| [`docs/08-glossary.md`](docs/08-glossary.md) | Glossary -- every coordinator word, in plain English |
| [`templates/pitch-letter-template.md`](templates/pitch-letter-template.md) | The one-email pitch with bracketed slots and fill-in notes |
| [`templates/day-of-checklist.md`](templates/day-of-checklist.md) | Printable day-of checklist: week before, thirty minutes before, the fifty minutes, clean-up |
| [`templates/repeatable-kit-inventory.md`](templates/repeatable-kit-inventory.md) | The printable kit inventory: box, four folders, and the one-page visit file |

## How to run it

Requires only Python 3 (standard library -- no installs, no network).

```bash
python3 scripts/build.py            # build the site into site/
python3 scripts/build.py --out DIR  # build somewhere else
python3 scripts/build.py --check    # lint the Markdown (links, anchors, structure)
python3 scripts/build.py --serve    # build, then preview on localhost
```

Then open `site/index.html` in any browser: a landing page, one
polished page per chapter and template with sidebar navigation and
prev/next pagers. The pages embed their stylesheet, make no external
requests, and open fine from `file://` or a USB stick -- which is
fitting, because the kit itself is designed to live on one.

## Tests

```bash
python3 -m unittest discover -s tests
```

The suite covers the Markdown converter, doc lint, the site builder,
the CLI, required-topic coverage (pitch, fifty minutes, accessibility,
A/V, selling, thank-yous, kit), and repo hygiene: no secrets anywhere,
the exact license line, and the README credit.

## How it differs from the sibling handbooks

- *author-newsletter-handbook* is what happens **between** visits: the
  reader email list, welcome sequences, archiving. Mention your
  newsletter at the visit; read that handbook for the send-and-keep
  half. The two projects deliberately share nothing but a pointer.
- *kickstarter-campaign-handbook* is for **crowdfunding the book**. A
  visit is not a funding ask: venue staff host, they do not back. No
  chapter here touches pledges.

## Honesty, labeled

- Everything in this manual works in the real world of folding tables
  and temperamental projectors; nothing requires paying for anything.
- Where a number is a rule of thumb (8-10 weeks lead time, 900-1,100
  words of reading), it says so.
- Sales tax and store margin rules vary; the manual tells you whom to
  ask rather than pretending one page of law fits every state.
- The manual contains no medical, legal, or tax advice; it is an
  event-planning handbook from one working author to another.

## License

MIT. Copyright (c) 2026 Asdale Dynamics, LLC -- see `LICENSE`. Copy,
adapt, print, and share freely; if it earns you one library evening of
new readers, we'd love to hear about it.
