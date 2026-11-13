# Legend of Gevievre — Gameplay & Systems Programming

> **Note:** This repository serves as a portfolio showcase for my personal contributions. To view the full project and source code, visit the [main repository](https://github.com/MagnierHugo/LegendOfGevievre).

## Overview
A 2D survivor-like game built in 42 hours for the "It's not a bug, it's a feature!" Game Jam in November 2025. The core experience revolves around intentionally broken mechanics, turning frustrating bugs—such as simulated network lag and loss of player control—into a chaotic and highly engaging core loop.

## Project Context
- **Role:** Gameplay Programmer & Technical Lead
- **Tech Stack:** Unity / C#
- **Team Size:** 7 Developers, 1 Artist
- **Development Time:** 42 Hours

## Core Systems & Architecture

### System A: Modular, Data-Driven Weapon Framework
Hardcoding distinct weapon behaviors during a 48-hour jam leads to technical debt. I needed to provide a scalable way to rapidly prototype bizarre weapons without breaking the main loop.
- **Scalable Architecture:** Architected a modular weapon framework that supported 3 distinct leveling tiers for every item.
- **Data-Driven Upgrades:** Separated weapon logic from stats, allowing behavior shifts and damage scaling to be mapped cleanly. This extensibility enabled junior team members to safely plug in new weapons without touching the core combat manager.

### System B: State Management & Intentional "Bugs"
Implementing mechanics that explicitly strip player agency without causing actual soft-locks or breaking hit detection.
- **State Transitions (The Scythe):** Engineered a robust state machine for the player character. Collecting a "Big XP Bubble" triggers a "Kidnap" mechanic, safely transitioning the player out of the "Controlled" state, suspending input velocity, and then seamlessly returning control.
- **Manipulating Physics (The Bow):** Programmed custom projectile behavior to simulate bad network lag. The logic utilizes intermittent velocity stops and stutters mid-flight while keeping the underlying hit-box detection perfectly accurate.
- **Economy & Pooling:** Built the underlying XP economy, handling instantiation, object pooling, and global event logic (e.g., the Magnet power-up overriding standard attraction vectors) to maintain performance with hundreds of gems on screen.

## Cross-Discipline Pipeline & Mentorship

- **Technical Leadership:** Mentored 1st and 2nd-year programming students throughout the jam. Conducted code reviews, debugged their systems, and managed the Git repository to resolve merge conflicts and protect the main branch.
- **Art Integration:** Acted as the technical bridge for the 2D artist. Integrated sprites, adjusted pivot points, and managed animation state transitions to ensure visual assets functioned correctly within the engine's logic.

## Key Engineering Takeaways
- **Programming "Badly" on Purpose:** Engineering mechanics like network stutter required a precise understanding of frame-perfect hit detection to ensure the bugs were frustratingly fun rather than genuinely game-breaking.
- **Architectural Scalability:** Establishing a clean, extensible framework in the first few hours of a jam was critical. It allowed me to delegate tasks safely and step into a mentorship role to keep the team synchronized under a tight deadline.
