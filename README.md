Snake Game
A modern take on the classic Snake game, built with HTML5, CSS, and JavaScript using the Canvas API. The game features a snake with a distinct head and eyes, multiple food types with effects, obstacles, level progression, a high score leaderboard, and mobile-friendly controls.
Features

Gameplay Mechanics:

Multiple Food Types:
Red (strawberry): +10 points.
Blue (square): Slows snake speed (+50ms, max 300ms).
Orange (triangle): Speeds up snake (-50ms, min 50ms).


Obstacles: Brown squares spawn each game (1 per level, max 5), with a 3-tile buffer zone around the snake's head to prevent unfair deaths.
Level Progression: Every 50 points, the level increases, adding obstacles and increasing speed (minimum 50ms interval).
Smooth Direction Queuing: Inputs are queued (max 2) to prevent missed taps/swipes, with debouncing to avoid reversing into the snake's body.


UI/UX:

Game Over Modal: Displays score, high score, and leaderboard. Allows entering 1-3 initials to save scores, with "Restart" and "Main Menu" buttons.
Countdown Timer: 3-2-1-Go! animation before starting or resuming the game.
Level Indicator: Shows current level above the canvas.
High Score Leaderboard: Stores top 5 scores with initials in local storage, displayed in the game over modal.


Mobile Experience:

Touch Controls: Swipe left/right to turn, up/down to pause/resume.
Larger Buttons: Bigger buttons on screens <400px for better touch targets.
Haptic Feedback: Vibrates on food eat (100ms) and death (200ms) if supported.


Visuals:

Snake Design: Green gradient body with a darker head and white eyes with black pupils, oriented by direction.
Food Animation: Strawberry shrinks/expands when eaten.
Responsive Design: Canvas scales to 90% viewport width on screens <600px, with adjusted font/button sizes.


Performance:

Uses requestAnimationFrame with timestamp deltas for smooth animation.
Debounced input to prevent rapid direction changes.



Setup Instructions

Download the Game:

Copy the index.html file to your local machine or a web server.


Run the Game:

Open index.html in a modern web browser (e.g., Chrome, Firefox, Safari).
No additional dependencies or server setup are required, as the game runs entirely in the browser.


Optional Hosting:

To play online, host index.html on a web server (e.g., GitHub Pages, Netlify, or a local server like http-server).



How to Play

Starting the Game:

Click the "Start Game" button to begin.
A 3-2-1-Go! countdown will start, then the snake moves right automatically.


Controls:

Desktop:
Left Button: Turn 90° counterclockwise.
Right Button: Turn 90° clockwise.
Straight Button: Continue in current direction.
Pause Button: Toggle pause/resume.


Mobile:
Swipe left: Turn counterclockwise.
Swipe right: Turn clockwise.
Swipe up/down: Toggle pause/resume.
Use on-screen buttons for the same actions.




Objective:

Eat food to grow and score:
Red (strawberry): +10 points.
Blue (square): Slows snake.
Orange (triangle): Speeds up snake.


Avoid hitting walls, the snake’s body, or obstacles.
Every 50 points, the level increases, adding obstacles and speeding up the snake.


Game Over:

On death, a modal shows your score and high score.
Enter 1-3 initials to save your score to the leaderboard.
Choose "Restart" to play again or "Main Menu" to reset.



Technical Details

Technologies: HTML5 Canvas, CSS, JavaScript.
Canvas Size: 400x400 pixels, divided into a 20x20 grid (20px per tile).
Base Speed: 200ms per move, adjustable via food effects and level progression.
Storage: Uses localStorage for high scores and leaderboard (top 5 entries).
Responsive Design: Scales for mobile devices, with larger buttons on screens <400px.
Animation: Uses requestAnimationFrame for smooth rendering, with delta-time-based updates.

Limitations

No audio effects (would require external .mp3 files).
No power-ups, snake growth animation, or theme switcher to keep the game lightweight.
Single-file structure (not modularized) for simplicity.
No endless mode or black (game-ending) food to maintain balanced gameplay.

Future Improvements

Add sound effects for eating, collisions, and level-ups (with toggle option).
Implement power-ups (e.g., shield, magnet, teleport).
Add a dark mode toggle and additional themes.
Modularize code into separate JS files (e.g., gameEngine.js, ui.js).
Introduce an endless mode without obstacles.

License
This project is unlicensed and provided as-is for educational purposes. Feel free to modify and distribute.
Acknowledgments

Built with inspiration from classic Snake games.
Enhanced based on user feedback for better gameplay, visuals, and mobile support.
