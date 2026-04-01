# Design Review Feedback – Battleship Game Sketches

The hand-drawn wireframes of the Battleship game, including the start screen, ship placement screen, gaming screen, result screen, and restart confirmation screen, were exhibited to players at a review session. Reviewers were invited to engage conceptually with the design and offer comments on its usability, clarity, completeness, and viability.


## Reviewer 1:

### Clarity of Feedback
- The named rows (A–J) and columns (1–10) in the grid arrangement made it extremely easy to see and very clear.
- Players were successfully distinguished by the usage of colors (🔴and🔵).
- Suggested making labels on the gaming screen more understandable, such as "Your Board" and "Opponent Board."

### Usefulness
- The placement → assault → outcome gameplay cycle was simple to understand.
- To prevent misunderstandings during games, it was suggested to provide a visual turn signal (such as "🔴 Red Player Turn").

### Suggested Improvements
- Added labels for both grids in the gameplay screen.
- Included a clear turn indicator at the top of the gameplay screen.


## Reviewer 2:

### Clarity of Feedback
- The start screen, placement screen, gaming screen, result screen, and restart confirmation were all included. 
- Because it stops inadvertent activities, the restart confirmation screen was welcomed.

### Consistency
- Every screen has the same design elements (buttons, boxes, and grids). 
- To improve visual uniformity, it was suggested that all buttons be the same size and shape.

### Suggested Improvements 
- Standardized button position and sizes on every screen. 
- Enhanced readability with greater UI element spacing.


## Reviewer 3 

### Comments on Usability 
- The positioning of ships is clearly displayed on the ship placement screen. 
- Suggested putting brief, straightforward directions on the screen, like "Ships must not overlap" (which was partially added). 

### Scalability 
- Future features like AI mode and difficulty selection can be added thanks to the layout.
- Suggested making room on the start screen for extra buttons or functionality. 

### Suggested Improvements
- Brief guidelines for ship placement (no overlap, inside grid) have been included. 
- Layout was changed to accommodate future feature growth.


## Reviewer 4 

### Technical Viability 
- Using common programming approaches, the concept is practical and easy to implement.
- Common data structures are well-aligned with the grid-based architecture. 

### Security-Related Issues
- Recommended making sure repeated moves are avoided by the system. 
- Recommended for verifying every user input (ship placement, grid limits). 

### Suggested Improvements
- Design comments included validation rules (no duplicate motions, correct coordinates). 
- Made sure the limitations on ship location are well-defined.


## Overall Strengths of the Design
1. A well-organized and transparent grid system
2. Powerful graphic depiction of ships and assaults
3. Full coverage of every state in the game
4. Effective use of symbols and color for clarity
5. User flow that is intuitive and logical
6. An overview of the changes made


## Improvements Made

The following improvements were implemented in response to the input received:

- "Your Board" and "Opponent Board" labels were added.
- A turn indication (🔴/🔵 Player Turn) was included.
- uniform button dimensions and placement
- Increased uniformity in layout and spacing
- Ship placement regulations now include more precise instructions.
- Added validation guidelines for inputs and movements
- Restart confirmation ensures that unintentional acts are avoided.
