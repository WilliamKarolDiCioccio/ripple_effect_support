# Ripple Effect — support

This is where bugs, questions and feature requests for
**[Ripple Effect](#what-ripple-effect-is)** go. It carries the issue templates,
the discussions and the licence — and nothing else. The application's source is
private and lives elsewhere.

| I want to… | Go here |
| --- | --- |
| Report something broken | [New bug report](../../issues/new?template=bug_report.yml) |
| Ask for a feature | [New feature request](../../issues/new?template=feature_request.yml) |
| Ask a question, or show what you made | [Discussions](../../discussions) |
| Check whether it is already known | [Open issues](../../issues) |

The app has a **support button** in its title bar that opens the right form
here with your version and operating system already filled in. It saves the two
questions every report otherwise starts with.

## What Ripple Effect is

A desktop application for writing interactive stories as graphs, inspired by
[ArcWeave](https://arcweave.com). You lay passages out on a canvas, wire each
choice to what it leads to, and press play to walk the result — with a visual
scripting layer around it (loops, conditions, arithmetic, random rolls and
restricted Python) so a story can compute as well as branch.

It is aimed at tabletop prep, game design documents, quest and dialogue trees,
and anything else where the interesting part of a document is the paths through
it.

A few things worth knowing before filing anything:

- **A project is a view onto a folder.** The app writes no scaffold and imposes
  no layout. Boards are `*.graph.json`, components are `*.component.json`,
  prose is ordinary Markdown and scripts are ordinary `.py` — all of it
  readable by anything else you own, and all of it meant for version control.
- **Python is not CPython.** Scripting runs on
  [monty](https://github.com/pydantic/monty), a restricted subset compiled to
  Rust. There is no `import requests`, no `class` and no `random`. The sandbox
  panel inside the app asks the interpreter what it can do rather than
  describing it, and it is the authority — not this paragraph.
- **The node editor is public.**
  [`fl_nodes_v2`](https://github.com/WilliamKarolDiCioccio/fl_nodes_v2) is a
  standalone package developed alongside the app, and it takes issues and pull
  requests of its own. If what is wrong is the canvas — panning, wiring,
  selection, undo — it may belong there instead.

## Getting a build

Ripple Effect ships as `.deb` and `.rpm` for Linux, `.msix` for Windows and a
universal `.dmg` for macOS. Builds are not published from this repository. If
you are looking for one, ask in [Discussions](../../discussions).

Nothing is code-signed yet, so Windows SmartScreen and macOS Gatekeeper both
want to be told the app is fine. Linux needs glibc 2.34 or newer — Ubuntu
22.04, Debian 12, Fedora 36, RHEL 9 and anything more recent.

## Filing a good bug

Most of a useful report is three lines:

1. **What you did** — the steps, from opening the app.
2. **What happened.**
3. **What you expected instead.**

Beyond that, the two that save a round trip are the **version** (About box, or
the app's support button fills it in) and whether it reproduces on a **fresh,
empty project**. If a specific project triggers it and you are able to share
it, a zipped folder is the single most useful thing you can attach — everything
in one is a plain text file you can read before you send it.

Please do not paste anything private into an issue. This repository is public,
and so is everything filed in it.

## Licence

Ripple Effect is proprietary software — see [LICENSE](LICENSE). It is not open
source. You may install and run the official builds for any purpose, personal
or commercial, and everything you author with it is yours; you may not
redistribute, modify or reverse engineer the software itself.

The dependencies it is built on stay under their own licences. The complete
list is in the app, under **About → Third-party licences**.

© 2026 William Karol Di Cioccio. All rights reserved.
