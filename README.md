# Project_Red_Hood

Developed with Unreal Engine 5.6.0

Based on the course Unreal Engine 5 Blueprints - The Ultimate Developer Course by Stephen Ulibarri  

Project Redhood is a playable side-scrolling dungeon crawler game built entirely in Unreal Engine 5 using Blueprints. In this game, players control Redhood, a nimble and powerful rogue who fights through skeleton enemies using a three-stage combo system. The game features moment-to-moment combat, hit feedback, enemy AI, and responsive controls.

## 🎮 Core Features

- **Sprites, Flipbooks, and Animation (PaperZD)**
  - PaperZD Animation Blueprints: Used to manage complex animation state machines (idle, run, attack, death) with clean transitions.
  - Sprite Flipbooks: Each animation (walk, idle, attack 1–3, hit, death) was crafted using flipbooks for frame-by-frame control.
  - Event-Driven Animation: Attack combos and damage responses are driven by animation notifies and transitions, syncing visual feedback with gameplay logic.
  - Alive State Management: Enemies use an `IsAlive` boolean in the animation blueprint to transition to the death animation and freeze the last frame.

- **Player Combat System**
  - Three-stage melee combo system with animation transitions
  - Accurate hit detection using custom box trace logic
  - Responsive attack buffering and canceling system
  - using UE5 enhanced input System

- **Enemy AI System**
  - Patrol, chase, and attack behaviors using Behavior Trees
  - Custom decorators and tasks to reach desired behaviors
  - Smooth rotation to face the player
  - Damage reception and hit reactions with animation syncing

- **Health and UI**
  - Dynamic health bars for enemies displayed above heads
  - Custom widget and overlays for more visual presentations
  - Floating damage numbers that reflect real-time combat output for player and enemies

- **Visual and Audio Feedback**
  - Niagara-based hit effects for enemy damage
  - Death animations that blend with state machine transitions
  - Sound effects for all attacks, hits, swipes, and enemy deaths
  - MetaSounds used for audio variation and attenuation

- **Death and Cleanup Logic**
  - Enemies stop all behavior and animation logic on death
  - Collision and UI visibility disabled upon death
  - Delayed self-destruction with optional idle corpse state

- **Polish and Best Practices**
  - Clean Blueprint architecture using base classes
  - Animation state machines for both idle/movement and death
  - Modular, scalable code with reusable components and widgets

## 🛠️ Tools & Technologies

- Unreal Engine 5.6.0 (Blueprint only)
- Niagara VFX for impact effects
- MetaSounds system for advanced audio control
- Behavior Trees and Blackboards for enemy AI
- Widget Components for 2D screen-space UI  
