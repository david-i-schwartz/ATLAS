# Skill tree

One small data file per lesson. Together they are the skill tree: what each lesson needs, what it teaches and where it came from.

**Status: no lessons listed yet.** The format below is a proposal.

The picture of the tree, the site's navigation and the list of what to build next are all generated from these files, so the tree is never drawn by hand.

## Proposed format

```yaml
id: collision.sphere-sphere
title: Sphere and sphere collision test
track: concepts            # concepts, graphics or cpp
requires:                  # ids of lessons to do first
  - math.vectors
  - physics.timestep
teaches:
  - distance test between two spheres
sources:                   # original repositories this lesson came from
  - IGME-RIT/physics-sphereCollision-3D-VisualStudio
status: todo               # todo, in progress, in review or done
```

## Rules

- `requires` lists only direct needs. If A needs B and B needs C, A does not list C.
- A lesson with no `requires` is a starting point.
- A topic the original material never covered still gets a file, with empty `sources` and `status: todo`, so gaps show up in the tree.
