---
title: "Dungeon Crawler — 2D JavaFX Game"
date: 2025-01-01
draft: false
description: "A 2D dungeon crawler built with JavaFX where players fight through waves of enemies, face bosses, and unlock upgrades as they progress through levels."
tags: ["Java", "JavaFX", "game-dev", "OOP"]
weight: 1
---

## Overview
Built a fully playable 2D dungeon crawler game in Java using JavaFX. Players choose a class, survive escalating waves of enemies, and face powerful boss encounters every 3 levels. The game features a progression system where difficulty scales with each level — faster enemies, larger waves, and tougher bosses with guard formations.

## Tech Stack
- **Language:** Java
- **Framework:** JavaFX
- **Rendering:** Canvas-based via GraphicsContext
- **Game Loop:** AnimationTimer running at ~60fps

## Classes & Gameplay
Players choose between two classes at the start:
- **Archer** — fires arrows, unlocks a 3-arrow spread shot at Level 3
- **Ninja** — throws spinning shurikens, unlocks a 3-shuriken spread shot at Level 3

Enemies march across the screen firing bullets at the player. Every 3rd level replaces normal waves with a boss encounter — a super enemy twice the normal size, surrounded by a 5×6 guard formation.

## Features
- Two playable classes with unique weapons and Level 3 upgrades
- Wave-based progression system that scales enemy count and speed per level
- Boss encounters every 3 levels with full guard formations
- Player health restored to 100 at the start of each new level
- Username displayed above the player character during gameplay

## Architecture & Design Patterns
- Abstract class hierarchy — `Player` → `Archer` / `Ninja`, `Enemy` → `SuperEnemy`
- Polymorphism used for player and enemy behaviors
- Iterator-safe collision detection
- Clean separation of concerns across 6 core files

## What I Learned
- Building a real-time game loop with JavaFX's AnimationTimer
- Applying OOP principles like abstract classes and polymorphism in a practical project
- Managing game state, collision detection, and progressive difficulty scaling
- Structuring a multi-class Java project cleanly from the ground up

## Links
- [GitHub Repository](https://github.com/JJ-Gillis23/Dunegon-Crawler-Game)