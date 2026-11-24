# ATLAS

Game programming tutorials and examples from RIT's School of Interactive Games and Media, being rebuilt into one connected tutorial.

**Status: early skeleton.** No lessons have been rebuilt yet.

## What this is

ATLAS began in 2016 as a collection of small, focused examples for learning game programming in C++: the language, math, graphics, physics, collision detection, data structures and algorithms. The originals are spread across about 720 repositories in the [IGME-RIT](https://github.com/IGME-RIT) organization, with an index at [bit.ly/programgames](https://bit.ly/programgames).

This repository rebuilds that material as a single tutorial. Every lesson states what it needs and what it teaches, so the lessons form a skill tree you can follow from the basics to any topic.

## How it is organized

The tutorial has three tracks that work together, plus the C++ language lessons.

| Track | What it covers |
|---|---|
| Concept lessons | Physics, math, collision, data structures and AI. They draw through the graphics core and contain no graphics API code, so each lesson can focus on its idea. |
| Graphics core | One small API for shapes, cameras, input and time. It runs on two engines: openFrameworks and a Vulkan core. |
| Graphics path | Lessons that open the core up and teach how it works, in Vulkan. |
| C++ language | Console programs that teach the language itself. |

| Folder | Contents |
|---|---|
| [`core/`](core/) | The graphics core and its two engines |
| [`lessons/`](lessons/) | The lessons, by track |
| [`tree/`](tree/) | The skill tree: one small data file per lesson |

## Where the original material is

The IGME-RIT organization stays as the archive, unchanged. Each rebuilt lesson links to the original repositories it came from.

## Credits and licence

The original examples were written by RIT students, supervised by David I. Schwartz. Source files name their authors, and rebuilt lessons keep those credits.

ATLAS is licensed under the GNU General Public License, version 3 or later, the same licence as the original examples. See [`LICENSE`](LICENSE).
