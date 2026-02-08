# Legend of Gevievre — Gameplay & Systems Programming

**Game Jam:** *It's not a bug, it's a feature!* (November 2025)

This repository serves as a portfolio showcase for my personal contributions to **Legend of Gevievre**, a 2D survivor-like game where mechanics are intentionally broken to create chaotic gameplay.

> [!IMPORTANT]
> **This is a showcase repository.**
> **[Click here to view the Full Project & Source Code](https://github.com/MagnierHugo/LegendOfGevievre)**

---

## Technical Contributions

### Modular Weapon & Upgrade System
I architected the core modular framework used for all weapons in the game, focusing on scalability and ease of iteration during the 48-hour deadline.
* **Leveling Logic:** Built a scalable system supporting 3 distinct tiers for every weapon.
* **Upgrade Mapping:** Implemented a data-driven approach to handle stat changes and behavior shifts as players level up.
* **Extensibility:** The system allowed the team to quickly implement new "buggy" weapon ideas without modifying the core combat loop.

### Gameplay Programming
I was responsible for the end-to-end implementation of specific weapons and core game loops.

**The Scythe (High Risk / High Reward)**
* Designed the logic where standard XP drops are replaced by "Big XP Bubbles."
* **Mechanic Implementation:** Programmed the "Kidnap" effect—when a player collects a Big Bubble, they temporarily lose control of their movement character.
* **State Management:** Ensured the player state correctly transitioned between "Controlled" and "Kidnapped" without breaking the game loop.

**The Bow (The "Lag" Mechanic)**
* Programmed a custom projectile behavior that simulates network lag.
* Utilized intermittent velocity stops and stutters mid-flight to mimic a bad internet connection while maintaining hit detection accuracy.

**XP Economy & Progression**
* Developed the underlying economy for experience points.
* Handled the instantiation, pooling, and collection logic for XP drops from enemies.

---

## Team Leadership & Design

### Mentorship
As a 3rd-year student working with 1st and 2nd-year developers, I took on a technical leadership role:
* **Code Reviews:** Helped junior team members debug their systems and integrate their work into the main branch.
* **Guidance:** Assisted in solving merge conflicts and architectural blockers.

### Game Design
* **Concept:** Co-designed the "intended bugs" for the entire arsenal, ensuring the mechanics were frustratingly fun rather than just broken.
* **Balancing:** Tuned the frequency of the "Kidnap" mechanic to ensure it remained a challenge rather than a soft-lock.

---

## Visuals

![GIF PLACEHOLDER: Showcase of the Scythe Kidnap mechanic or Bow Lag]

---

## Key Takeaway
This project challenged me to **program "badly" on purpose**. It required a deep understanding of how "correct" systems work in order to break them in ways that remained fun and performant. It also allowed me to step into a mentorship role, ensuring the team stayed synchronized under a tight deadline.
