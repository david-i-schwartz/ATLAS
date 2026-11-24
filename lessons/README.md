# Lessons

**Status: no lessons yet.**

## Tracks

| Folder | Track | Draws with |
|---|---|---|
| `lessons/concepts/` | Physics, math, collision, data structures, AI | The graphics core only |
| `lessons/graphics/` | The graphics path: how the core works | Vulkan |
| `lessons/cpp/` | The C++ language | Nothing; console programs |

## Proposed layout of one lesson

This layout is a proposal until the first pilot lessons settle it.

```
lessons/concepts/collision-sphere-sphere/
  README.md     the lesson page: the idea, the code walked through, what to try
  src/          the lesson's code
  tests/        tests that check the idea
```

Each lesson also has a data file in [`tree/`](../tree/) that says what it requires and what it teaches.
