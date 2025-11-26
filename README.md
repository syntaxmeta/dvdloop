# dvdloop
The Perfect Corner DVD Screensaver This project is a sophisticated, interactive tribute to the classic DVD logo screensaver, engineered using HTML, CSS, and JavaScript. It replicates the mesmerizing, random movement of the logo across the screen while adding modern flair and a unique challenge.

✨ Key Features and Technologies
1. Dynamic Visuals (HTML & CSS)
Bouncing Element: A specific image (#dvd-logo) is absolutely positioned and sized to simulate the classic DVD player logo.

Neon Glow and Color Cycling: The logo uses CSS filter: drop-shadow() to give it a vibrant, neon appearance. This glow color changes every time the logo collides with a wall, using a predetermined COLOR_CYCLE.

Animated Background: The background is not static. It features a pulsating, deep-space ripple effect created by a CSS radial-gradient within a @keyframes animation.

Synchronized Theme: Crucially, the background's animated gradient colors also change simultaneously with the logo's glow color, making the entire screen pulse with a single, synchronized theme.

2. Core Motion and Physics (JavaScript)
Real-time Animation Loop: The logo's movement is handled by the browser's optimized window.requestAnimationFrame() function, ensuring smooth, fluid motion that adapts to the user's screen refresh rate.

Boundary Collision: The JavaScript calculates the logo's position (x, y) and velocity (dx, dy) in pixels per frame. When the logo's edge reaches the container boundaries (.visual-container), the corresponding velocity is reversed (dx = -dx or dy = -dy), simulating a perfect bounce off the wall.

Speed Control: A constant SPEED variable allows for easy adjustment of the logo's travel velocity.

3. Interactive Challenge (The Corner Counter)
The project includes a unique, challenging feature that tracks a rare event: the Perfect Corner Hit.

Detection Logic: The code uses two collision flags (collidedX and collidedY). A "perfect corner" is registered only when both flags are true in the same animation frame, meaning the logo simultaneously reversed its direction on the X-axis and the Y-axis.

Tracking and Timing:

A Perfect Corners counter tracks the total number of successful corner hits.

A high-precision timer uses performance.now() to measure and display the exact time interval (down to milliseconds) between consecutive perfect corner hits.

Feedback: When a perfect corner is achieved, the logo briefly flashes larger (scale(1.1)) for dramatic emphasis.
