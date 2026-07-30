# Project Overview

This is a self-contained browser game built in a single file: `index.html`.
It uses an HTML canvas and plain JavaScript—there is no package manager, build
step, or external runtime required.

## Gameplay Systems

- **Root phase:** Guide a tree root downward, collect water and minerals, avoid
  hazards, and unlock additional tree types by reaching depth milestones.
- **Trees:** Oak, Apple, and Pear have distinct root and tower-defense bonuses,
  growth materials, and tech trees.
- **Tower defense:** On root death, defend the tree from enemy waves with acorn
  turrets. Players can unlock more turrets, change turret targeting/type, and
  plant runner saplings for vision.
- **Resources:** Water, minerals, and tree-created materials pay for growth,
  runner saplings, and root/defense upgrades.

## Working Guidelines

- Keep gameplay logic, input handling, rendering, and game-state changes in
  `index.html` consistent with one another.
- The canvas coordinate system is `900 × 680`; tower-defense panning uses
  `td.viewOffset`, so convert screen clicks to world coordinates when adding
  TD interactions.
- Use `git diff --check` after edits. There is currently no Node.js toolchain
  or automated test suite in this repository.
- Do not add dependencies or a build system unless explicitly requested.
