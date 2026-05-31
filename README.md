# CoinFlipSim
## About
This is a text-based game consisting of a gameplay loop of flipping a coin and purchasing upgrades that enhance various attributes of the system, with the goal of achieving 10 consecutive heads.

This program was originally developed in Google Colab, but has since been refactored to improve portability and usability. It now runs in most standard Python environments without requiring external dependencies such as Google Drive mounting.

The main highlights of this program are the coin flipping animation, the state-based menu system, and the save file functionality. These features are designed to loosely emulate progression and interaction systems found in modern incremental games.

## Attribution
This game was inspired by an existing game, 'Unfair Flips', which was created by Heather Flowers. The core philosophy was inspired by that game, but adapted into a text-based implementation.

Original Game: [Unfair Flips Steam Page](https://store.steampowered.com/app/3925760/Unfair_Flips/)

## How the game works
- The objective of this game is to flip a coin and achieve 10 consecutive heads. Initially, the odds are heavily unfavourable, making success difficult without upgrades.
- Each successful heads flip grants in-game currency, which can be spent on upgrades such as coin flip speed, probability of heads, base reward value, and a streak-based multiplier system.
- The game loop involves repeated flipping and upgrading until the probability conditions become favourable enough to reach the objective.
- As the system is probability-based, outcomes vary significantly; the game can be completed with minimal upgrades or may remain challenging even after extensive progression.

## Core systems
- **Menu State System**
  - The game is structured around a state-based menu loop
  - Players transition between main menu, gameplay, and upgrade shop
  - Each state handles input validation and controlled exits to prevent invalid flow

- **Game Feedback & Animation System**
  - Coin flipping uses timed ASCII animation frames
  - Built using controlled delays (`time.sleep`) and screen clearing for visual feedback
  - Designed to prevent the game from feeling like a purely random process by visually representing outcomes and upgrade effects such as reduced flip time

- **Save & Persistence System**
  - Game state is stored in a structured JSON save file
  - Supports loading existing progress or creating a new save
  - Includes error handling for missing or corrupted save files
  - Refactored from Google Colab Drive-based storage to local filesystem for portability

## How to run the game
- Install Python
- Run coin_flip.py
