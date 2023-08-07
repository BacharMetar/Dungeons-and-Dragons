# Dungeons and Dragons Game - README

## Table of Contents
1. [Overview](#overview)
2. [Game Description](#game-description)
3. [Game Flow](#game-flow)
   - [Game Board](#game-board)
4. [Game Tiles](#game-tiles)
   - [Range](#range)
   - [Units](#units)
   - [Player](#player)
   - [Player Types](#player-types)
   - [Enemies](#enemies)
      - [Enemy Types](#enemy-types)
5. [Combat System](#combat-system)
6. [The CLI (Command Line Interface)](#the-cli-command-line-interface)
   - [Interacting with the CLI - Callbacks/Observer Pattern](#interacting-with-the-cli---callbacksobserver-pattern)
7. [Forms of Input](#forms-of-input)
8. [Testing Your Game](#testing-your-game)
9. [Bonus (+5 points each)](#bonus-5-points-each)
   - [Add New Player Class](#add-new-player-class)
   - [Add New Enemy Class](#add-new-enemy-class)
10. [Submission Guidelines](#submission-guidelines)

## Overview
This project implements a single-player multi-level version of a Dungeons and Dragons board game. Navigate through dungeons, defeat enemies, and advance through levels to win the game. The program adheres to OOP principles and coding conventions.

## Game Description
The game unfolds on a board featuring a player, various enemies, walls, and open areas. Different symbols represent these elements, with the player aiming to progress through levels by defeating enemies and surviving.

## Game Flow
The game consists of multiple levels. Each level comprises rounds, where the player and enemies take actions. Levels are completed by defeating all enemies. The game concludes when the player finishes all levels or is defeated.

### Game Board
The board is a 2D array of characters representing walls, characters, and free cells. Players and enemies move within this grid.

## Game Tiles
Tiles include empty cells, walls, and units (player and enemies). Each tile has properties like the tile character and its position.

### Range
The range between two points is defined by their Euclidean distance formula.

### Units
Units encompass both players and enemies. Each unit has attributes like name, health, attack points, and defense points.

### Player
Players have unique properties:
- Experience
- Player Level
Players can cast special abilities based on their class.

### Player Types
Three player classes exist: Warrior, Mage, and Rogue. Each has distinct abilities, resource management, and leveling.

#### Warrior
- Special Ability: Avenger's Shield
- Cooldown Period
- Level-Up Bonuses

#### Mage
- Special Ability: Blizzard
- Mana Management
- Spell Power

#### Rogue
- Special Ability: Fan of Knives
- Energy Resource
- Combat Strategy

### Enemies
Enemies include monsters and traps. They have specific behaviors, visibility, and attack patterns.

#### Enemy Types
Monsters and traps populate the game world, each with unique properties. Monsters can chase the player, while traps use visibility and invisibility cycles.

## Combat System
Combat occurs when a player or enemy enters a cell occupied by an enemy. Both attacker and defender roll dice based on attack and defense points. Damage is dealt and health may decrease.

## The CLI (Command Line Interface)
The game starts with player selection and displays the game state after each round. Players can perform actions like moving, casting abilities, and skipping turns.

### Interacting with the CLI - Callbacks/Observer Pattern
The UI and business layers communicate using callbacks or the Observer pattern.

