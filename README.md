# Legend of Gevievre — Gameplay & Systems Programming

> **Note:** This repository serves as a portfolio showcase for my personal contributions. To view the full project and source code, visit the [main repository](https://github.com/MagnierHugo/LegendOfGevievre).

## Overview
A 2D survivor-like game built in 42 hours for the "It's not a bug, it's a feature!" Game Jam in November 2025[cite: 4]. The core experience revolves around intentionally broken mechanics, turning frustrating bugs—such as simulated network lag and loss of player control—into a chaotic and highly engaging core loop[cite: 4].

## Project Context
- **Role:** Gameplay Programmer & Technical Lead[cite: 4]
- **Tech Stack:** Unity / C#[cite: 4]
- **Team Size:** 7 Developers, 1 Artist[cite: 4]
- **Development Time:** 42 Hours[cite: 4]

## Core Systems & Architecture

### System A: Modular, Data-Driven Weapon Framework
Hardcoding distinct weapon behaviors during a 48-hour jam leads to technical debt. I needed to provide a scalable way to rapidly prototype bizarre weapons without breaking the main loop[cite: 5].
- **Scalable Architecture:** Architected a modular weapon framework that supported 3 distinct leveling tiers for every item[cite: 5].
- **Data-Driven Upgrades:** Separated weapon logic from stats, allowing behavior shifts and damage scaling to be mapped cleanly[cite: 5]. This extensibility enabled junior team members to safely plug in new weapons without touching the core combat manager[cite: 5].

### System B: State Management & Intentional "Bugs"
Implementing mechanics that explicitly strip player agency without causing actual soft-locks or breaking hit detection[cite: 5].
- **State Transitions (The Scythe):** Engineered a robust state machine for the player character[cite: 5]. Collecting a "Big XP Bubble" triggers a "Kidnap" mechanic, safely transitioning the player out of the "Controlled" state, suspending input velocity, and then seamlessly returning control[cite: 5].
- **Manipulating Physics (The Bow):** Programmed custom projectile behavior to simulate bad network lag[cite: 5]. The logic utilizes intermittent velocity stops and stutters mid-flight while keeping the underlying hit-box detection perfectly accurate[cite: 5].
- **Economy & Pooling:** Built the underlying XP economy, handling instantiation, object pooling, and global event logic (e.g., the Magnet power-up overriding standard attraction vectors) to maintain performance with hundreds of gems on screen[cite: 5, 6].

## Cross-Discipline Pipeline & Mentorship

- **Technical Leadership:** Mentored 1st and 2nd-year programming students throughout the jam[cite: 6]. Conducted code reviews, debugged their systems, and managed the Git repository to resolve merge conflicts and protect the main branch[cite: 6].
- **Art Integration:** Acted as the technical bridge for the 2D artist[cite: 6]. Integrated sprites, adjusted pivot points, and managed animation state transitions to ensure visual assets functioned correctly within the engine's logic[cite: 6].

## Key Engineering Takeaways
- **Programming "Badly" on Purpose:** Engineering mechanics like network stutter required a precise understanding of frame-perfect hit detection to ensure the bugs were frustratingly fun rather than genuinely game-breaking[cite: 6].
- **Architectural Scalability:** Establishing a clean, extensible framework in the first few hours of a jam was critical[cite: 6]. It allowed me to delegate tasks safely and step into a mentorship role to keep the team synchronized under a tight deadline[cite: 6].
