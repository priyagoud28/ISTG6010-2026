# Battleship Game – Requirements and User Stories

## 1. 1. Overview
The specifications and user stories for a software-based Battleship game implementation are presented in this paper.
Clarity, accuracy, and testability were ensured by refining the criteria once they were obtained through an interview.

This article aims to prevent ambiguity in acceptance criteria while defining a precise and workable definition of the fundamental Battleship game.

**2. Synopsis of the Interview**

**2.1 Objective**
To learn about gaming guidelines, user expectations, and typical problems with the classic version of the game, an interview with a Battleship game specialist was undertaken.
The system requirements were guided by this information.

### 2.2 Key Questions and Responses

**Q1: How do you play Battleship?  

In the turn-based strategy game Battleship, 🔴 Red Player and 🔵 Blue Player arrange ships on a grid and alternately estimate locations to find and sink each other's ships.

**Q2: What are the main elements of the game**?

Every participant makes use of:One ship placement grid  
One grid to monitor assaults  
A turn-based combat mechanism and ships of various sizes are additional features of the game.

**Q3: What issues does the conventional version have?**  

Gamers could:- Losing track of prior estimates  
Repeat the actions  
Make mistakes when recording misses (🌊) and hits (💥).  
Confusion and unfair games may result from these problems.

**Q4: How may a software update enhance the game?**  

A digital system is capable of:Track moves automatically  
Avoid using incorrect or duplicate inputs  
Give precise feedback, such as hits (💥), misses (🌊), and sunk ships.  

**Q5: Which characteristics are crucial to users?** 

Key characteristics include of:The grid pattern is clear.  
Hit (💥) and miss (🌊) visual feedback  Simple ship placement  - A clear indicator of who's turn it is## 2.3 Important Results
The following crucial prerequisites were identified during the interview:Dual-grid tracking and gaming system  Automated rule enforcement (no overlapping ships, no duplicate moves)  Instantaneous visual feedback  
Turn-based, structured gameplay  
An easy-to-use interface  

The user stories and approval criteria listed below were influenced by these findings.

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
