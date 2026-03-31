# Battleship Game – Requirements and User Stories

## 1. Introduction
This document presents the requirements and user stories for a software-based implementation of the Battleship game.  
The requirements were gathered through an interview and refined to ensure clarity, precision, and testability.

The goal of this document is to define a clear and implementable specification of the core Battleship game while avoiding ambiguity in acceptance criteria.


## 2. Interview Summary

### 2.1 Purpose
An interview was conducted with a Battleship game expert to understand gameplay rules, user expectations, and common issues in the traditional version of the game.  
This information was used to guide the system requirements.


### 2.2 Key Questions and Responses

**Q1: How is Battleship played?**  
Battleship is a turn-based strategy game where 🔴 Red Player and 🔵 Blue Player place ships on a grid and take turns guessing coordinates to locate and sink each other’s ships.

**Q2: What are the key components of the game?**  
Each player uses:
- One grid for placing ships  
- One grid for tracking attacks  
The game also includes ships of different sizes and a turn-based attack system.

**Q3: What problems exist in the traditional version?**  
Players may:
- Lose track of previous guesses  
- Repeat moves  
- Make errors when recording hits (💥) and misses (🌊)  
These issues can lead to confusion and unfair gameplay.

**Q4: How can a software version improve the game?**  
A digital system can:
- Automatically track moves  
- Prevent duplicate or invalid inputs  
- Provide clear feedback such as hits (💥), misses (🌊), and sunk ships  

**Q5: What features are important for users?**  
Important features include:
- Clear grid layout  
- Visual feedback for hits (💥) and misses (🌊)  
- Easy ship placement  
- Clear indication of whose turn it is  


### 2.3 Key Findings
The interview revealed the following essential requirements:
- Dual-grid system for gameplay and tracking  
- Automated rule enforcement (no duplicate moves, no overlapping ships)  
- Immediate visual feedback  
- Structured turn-based gameplay  
- Clear and simple user interface  

These findings informed the user stories and acceptance criteria below.


## 3. Scope of the System

### 3.1 Core Features
The core version of the Battleship game includes:
- Two-player gameplay (🔴 Red Player vs 🔵 Blue Player)
- Ship placement on a 10x10 grid
- Turn-based attack system
- Hit (💥) and miss (🌊) feedback
- Ship-sunk detection
- Win condition detection
- Restart functionality

### 3.2 Out of Scope (Future Enhancements)
The following features are excluded from the core system:
- Single-player mode (AI opponent)
- AI difficulty levels


## 4. User Stories and Acceptance Criteria

### User Story 1: Ship Placement
**As the 🔴 Red Player or 🔵 Blue Player, I want to place my ships on a grid so that I can prepare for the game.**

#### Acceptance Criteria
- The system displays a 10x10 grid for ship placement.
- Ships can be placed only within grid boundaries.
- Ships can be placed horizontally or vertically.
- The system prevents overlapping ships.
- The system visually confirms each placed ship.
- The game does not start until all ships are placed.


### User Story 2: Attack Tracking
**As the 🔴 Red Player or 🔵 Blue Player, I want a separate tracking grid so that I can see my previous attacks.**

#### Acceptance Criteria
- The system displays a second 10x10 tracking grid.
- Each attack is recorded on the tracking grid.
- Hits (💥) and misses (🌊) are visually distinguishable.
- Previously attacked cells remain visible.
- The tracking grid does not reveal unhit ships.


### User Story 3: Making a Move
**As the 🔴 Red Player or 🔵 Blue Player, I want to select coordinates on my opponent’s grid so that I can attempt to hit their ships.**

#### Acceptance Criteria
- The player can select only coordinates within the grid.
- The system rejects coordinates that were already selected.
- The system records whether the result is a hit (💥) or a miss (🌊).
- The result is displayed immediately.
- After a valid move, the turn switches to the other player.

#### Definition of a Valid Move
A valid move is:
- A coordinate within the grid, and  
- A coordinate that has not been selected before.


### User Story 4: Move Feedback
**As a player, I want immediate feedback so that I understand the result of my move.**

#### Acceptance Criteria
- A hit is clearly indicated using 💥.
- A miss is clearly indicated using 🌊.
- A “ship sunk” message is displayed when all parts of a ship are hit.
- Feedback is shown immediately after each move.


### User Story 5: Turn Management
**As a player, I want to know whose turn it is so that gameplay remains organized.**

#### Acceptance Criteria
- The system identifies which player starts first.
- Only the current player can make a move.
- The turn switches after each valid move.
- The current player is clearly displayed (🔴 or 🔵).


### User Story 6: Winning the Game
**As a player, I want the game to end when all ships of one player are sunk so that the winner is clear.**

#### Acceptance Criteria
- The system tracks all ship positions for each player.
- The system tracks all successful hits (💥).
- The game ends when all ship positions of one player are hit.
- A winning message is displayed identifying the winner (🔴 or 🔵).
- No further moves are allowed after the game ends.


### User Story 7: Restarting the Game
**As a player, I want to restart the game so that I can play again.**

#### Acceptance Criteria
- A restart option is available.
- Restart clears both players’ boards.
- Restart clears all previous hits (💥) and misses (🌊).
- Restart resets turn order.
- Players must place ships again before starting a new game.


## 5. Conclusion
This document defines a clear and testable set of requirements for a Battleship game.  
Ambiguous statements have been replaced with precise, observable behaviors to improve clarity and evaluation.

By focusing on core functionality and separating advanced features into future enhancements, the system remains practical to implement and easy to assess.
