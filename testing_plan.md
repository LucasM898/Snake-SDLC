# Snake Game with Minecraft Texture Reskin Test Plan

## 1. Boundary Cases

### Number of Players
- **Test Data**: 1 player
- **Expected Outcome**: Game should accept 1 player in solo mode. The game should handle this mode without crashes or errors.

### Speed
- **Test Data**: Speed 1, Speed 10
- **Expected Outcome**: Snake should move at a constant speed at level 1, and the speed should progressively increase with each level, becoming faster as the player advances.

### Maximum Score
- **Test Data**: Maximum achievable score
- **Expected Outcome**: When the maximum score is reached, the game should cap the score without breaking. The score display should highlight the max score with a special effect, like a gold frame.

### Boundary Interaction
- **Test Data**: Snake movement near boundaries (left, right, top, bottom)
- **Expected Outcome**: When the snake hits the boundary, it should either end the game or wrap around to the opposite side (if the game supports wrapping). If wrapping is not supported, the game should show a "Game Over" message when hitting boundaries.

---

## 2. Design Integration

### Movement and Collision Testing
- **Test Data**: Snake moving in different directions, colliding with walls, or its own body.
- **Expected Outcome**: Snake should move within the boundaries of the play area. Collisions with walls or its own body should end the game. The snake should not pass through walls or other obstacles.

### Score and Level Integration
- **Test Data**: Clearing food, collecting power-ups.
- **Expected Outcome**: The score should increase correctly when food is eaten, and the level should increase as the score hits specific thresholds. Ensure proper level progression when the player eats a certain number of food items.

---

## 3. Unit and Logic Testing

### Snake Movement
- **Test Data**: Snake moving up, down, left, and right.
- **Expected Outcome**: The snake should move in the expected direction based on user input. It should not overlap with itself or move in the opposite direction (e.g., moving left when moving right).

### Scoring
- **Test Data**: Snake eating food, special items.
- **Expected Outcome**: The score should increment by a set amount when food is eaten. Special items should trigger additional effects like score multipliers or new abilities for the snake.

### Snake Growth
- **Test Data**: Snake length increases after eating food.
- **Expected Outcome**: After each piece of food is consumed, the snake should grow by 1 segment, and the gameplay should adapt to the increased length (e.g., slower movement or more difficulty avoiding obstacles).

---

## 4. Protect Execution from Bad Input

### Invalid Key Presses
- **Test Data**: Pressing multiple conflicting keys or invalid keys (e.g., pressing "W" and "S" at the same time).
- **Expected Outcome**: The game should ignore conflicting key presses, with no unexpected behavior or crashes. Only valid directional keys (Up, Down, Left, Right) should be responsive.

### Non-Numeric Input (for Score or Player Name)
- **Test Data**: Non-numeric values in score or name input.
- **Expected Outcome**: The game should gracefully handle non-numeric input when entering player names or any other text-based data, displaying an error message when necessary.

---

## 5. Handle Other Run-Time Errors

### Snake Colliding with Itself
- **Test Data**: Snake eating itself after growing long.
- **Expected Outcome**: If the snake collides with its own body, the game should end, displaying a "Game Over" message. The game should not freeze or cause lag in this scenario.

### Handling Full Screen or Unresponsive States
- **Test Data**: Play until screen is full or game is unresponsive.
- **Expected Outcome**: If the snake runs into itself or reaches the screen's edge, the game should display "Game Over." If the game crashes, it should not occur due to reaching a full screen or getting stuck in an infinite loop.

### Handling High-Speed Levels
- **Test Data**: Test game speed when the snake moves faster at higher levels.
- **Expected Outcome**: The snake should move faster as levels progress, without any performance lag or freezing.

---

## 6. Test Case Table

| Test Case                      | Test Data                          | Expected Outcome                                                                                       |
|---------------------------------|------------------------------------|-------------------------------------------------------------------------------------------------------|
| Player Count                    | 1 player                           | Game should accept 1 player in solo mode.                                                             |
| Snake Movement                  | Moving up, down, left, right       | Snake should move correctly and stop at boundaries or collide with itself for "Game Over".             |
| Score Increase                  | Eating food                        | Score should increase correctly based on food eaten and special items collected.                       |
| Snake Growth                    | Snake eating food                  | Snake length should increase by one segment after each food item is eaten.                             |
| Speed Increase                  | Level 1, Level 10                  | Snake should move faster as the player advances through levels, with appropriate speed scaling.        |
| Invalid Input                   | Pressing conflicting keys          | Game should ignore conflicting inputs and not crash.                                                   |
| Full Screen                     | Screen nearly full                 | Game should end and show a "Game Over" screen when the snake hits the top after eating too many foods.  |
| Save/Load                       | Valid and invalid save/load data   | Game should save and load correctly, with proper handling of corrupted data.                           |
| Snake Collision                 | Snake colliding with walls or itself | If snake hits wall or body, the game should end with "Game Over".                                      |
| Non-Numeric Input               | Invalid input for scores or names  | The game should handle non-numeric inputs gracefully, displaying appropriate error messages when needed. |
