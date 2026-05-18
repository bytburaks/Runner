# Endless Runner Game - Mobile Optimized 3D/2D Project

This repository contains an endless runner game developed using **Unity** and **C#**. The project focuses on high-performance endless world generation, smooth input controls, and scalable object-oriented design patterns, making it highly optimized for both mobile and PC platforms.

## 🚀 Play in Browser
You can play the web-optimized version of the game directly on your browser via GitHub Pages:
👉 **[Click Here to Play the Game](https://bytburaks.github.io/Runner/)**

---

## 🛠️ Tech Stack & Key Features

*   **Game Engine:** Unity
*   **Language:** C# (SOLID Principles, Event-Driven Architecture)
*   **Optimization:** Object Pooling System for obstacles, collectibles, and environment tiles.
*   **Generation:** Procedural endless level generation with progressive difficulty scaling.
*   **Input System:** Mobile-friendly swipe controls and standard keyboard inputs.

---

## ⚙️ Technical Highlights (What I Implemented)

### 1. High-Performance Object Pooling
*   Avoided runtime memory allocation (`Instantiate` and `Destroy` overhead) by creating a robust **Object Pooler**.
*   Recycled active platform tiles, obstacles, and collectible items dynamically, preventing garbage collection (GC) spikes and ensuring a locked 60 FPS performance on target mobile devices.

### 2. Procedural Endless Level Generation
*   Developed an algorithmic tile-spawning system that stitches environment segments seamlessly ahead of the player.
*   Implemented a **Progressive Difficulty Modifier** that increases the player's forward speed and decreases obstacle spawn intervals as the score increases.

### 3. Lane-Based Movement & Physics
*   Coded a precise lane-switching mechanic (Left, Center, Right) using smooth interpolations (`Mathf.Lerp` / `Transform.Translate`) rather than basic physics forces to ensure predictable and responsive gameplay.
*   Integrated custom gravity and jump curves to create a satisfying, arcade-like game feel (Juice).

### 4. Game Data & State Management
*   Designed a centralized `GameManager` utilizing the **Singleton Pattern** to handle game states (`MainMenu`, `Gameplay`, `GameOver`).
*   Implemented local high-score saving using Unity’s `PlayerPrefs` system, fully compatible with WebGL sandboxing.

---

## 🎮 Controls

*   **PC:** `A` / `D` or `Left` / `Right` Arrow Keys to switch lanes. `Space` or `Up Arrow` to jump. `S` or `Down Arrow` to slide.
*   **Mobile:** Swipe Left/Right to switch lanes, Swipe Up to jump, Swipe Down to slide.

---
