# Graphics core

One small API that every concept lesson draws through, so a lesson on collision or integration contains no graphics API code.

**Status: not started.** The function list is not decided yet.

## The idea

A lesson asks for simple things: open a window, draw a sphere here in this colour, move the camera, read a key, step time. The graphics core provides those calls and nothing lower-level.

Two engines sit underneath and provide the same calls:

| Engine | Folder | Notes |
|---|---|---|
| openFrameworks | `core/of/` | Used as released, not modified. |
| Vulkan core | `core/vulkan/` | A separate small engine built in this repo, starting from the ATLAS Vulkan tutorials. |

A lesson written against the core runs on either engine without changes.

## Not here

How the core works inside (buffers, shaders, pipelines, lighting) is taught on the graphics path, under `lessons/graphics/`.
