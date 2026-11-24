# ATLAS: rules for Claude Code sessions

Read this before doing anything in this repository.

## What this repo is

ATLAS is the rebuild of RIT IGM's game programming tutorials into one connected tutorial with a skill tree. The owner and reviewer is Dave (David I. Schwartz). The original material is about 720 repositories in `github.com/IGME-RIT`, indexed by two Google Docs:

- Main index: https://docs.google.com/document/d/1EKs9Ygo_ZQgcp35BbByWP6Qgha-rw2FpL-B5Bq4IchM/edit
- Physics Extras: https://docs.google.com/document/d/1nEZmMIvhlc_5_-0gXTH4BelhzFEg4vB3fk_TF0OucUc/edit

## Decisions already made

Do not reopen these without Dave.

- This repository is the home of the rebuild.
- Nothing from the original material is dropped for now.
- Concept lessons (physics, math, collision, data structures, AI) draw only through the graphics core. They never include or call OpenGL, Vulkan or openFrameworks directly.
- The graphics core is one small API with two engines underneath: openFrameworks and a separate Vulkan core that lives in this repo.
- openFrameworks is used as released. Do not fork it, patch it or write a renderer inside it. It wraps OpenGL, and that is accepted.
- OpenGL is not taught and not called by any lesson. Graphics topics are taught on the graphics path, in Vulkan.

## Not decided yet

Ask Dave. Do not assume an answer.

- The graphics core's function list.
- The build setup (Visual Studio solutions, CMake, or both), compilers and platforms.
- The lesson data file format (YAML is proposed in `tree/README.md`).
- Whether lessons also build for the browser.

## Sources

- The IGME-RIT organization is a read-only archive. Never push to it, and never rename, archive or delete anything there.
- When a topic has several copies, start from the copy the index links to. For physics that is usually the 2019 repo whose name ends in `-VisualStudio`.
- The originals carry their libraries and build output in the repo. Do not copy those in. Only source, shaders and assets a lesson needs belong here.

## How to work

- One lesson per session and per pull request.
- Lesson work goes on a branch and into a pull request for Dave. Do not push lesson work to `main`, and do not merge your own pull request.
- Port the idea, not the boilerplate. An original example is one large `main.cpp` that mixes window, shader and draw code with the idea being taught. The rebuilt lesson keeps the idea in plain C++ and draws through the graphics core.
- Keep the credits. Copy the original authors' names from the source header into the lesson, keep the GPL notice, and list the original repositories the lesson came from.
- When you find a bug in an original, fix it and record it in the lesson's notes: what was wrong and what you changed.
- Check physics and math against the original code or a reference, and name the reference. Do not state formulas from memory alone.
- Say what you ran. If something could not be built or tested in the session, say so in the pull request. Never describe a lesson as working unless you ran it.

## A lesson is done when

1. It builds.
2. Its tests pass, and the tests check the idea (for example, a collision test's known hit and miss cases), not only that the program starts.
3. Its page explains the idea in plain language, with terms defined on first use.
4. Its data file in `tree/` is filled in: what it requires, what it teaches, its sources and its status.
5. The pull request lists what was ported, what was fixed and what was not verified.
