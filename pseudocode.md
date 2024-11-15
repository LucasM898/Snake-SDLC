# Pseudocode for Minecraft-Themed Snake Game (Creeper Skin)

## Initialize Game

- Setup the grid to represent the game area.  
  - Create a snake as a list of grid positions with an initial length of 3.  
  - Apply a Creeper texture to represent the snake.  
  - Set the initial direction to "RIGHT" and score to 0.  
  - Place a random Minecraft food item (e.g., apple, bread, steak, golden carrot) on the grid.  

## Load Minecraft Assets

- Use Creeper texture for the snake segments.  
- Select Minecraft food textures to represent food items.  
- Set the game background to a Minecraft grass/dirt block pattern.  

## Game Loop

- Display the grid, Creeper snake, Minecraft food, and themed background.  
- Handle player input using arrow keys:  
  - Check if the input is "UP" and the direction is not "DOWN".  
    - If true, set the direction to "UP".  
  - Check if the input is "DOWN" and the direction is not "UP".  
    - If true, set the direction to "DOWN".  
  - Check if the input is "LEFT" and the direction is not "RIGHT".  
    - If true, set the direction to "LEFT".  
  - Check if the input is "RIGHT" and the direction is not "LEFT".  
    - If true, set the direction to "RIGHT".  

- Move the snake:  
  - Add a new head position based on the current direction.  
  - Remove the tail unless the snake eats food.  

- Check for collisions:  
  - If the snake’s head touches the grid boundary:  
    - End the game.  
  - If the snake’s head touches its own body:  
    - End the game.  

- Check if the snake eats food:  
  - If the snake’s head position matches the food’s position:  
    - Increase the score.  
    - Grow the snake by keeping the tail.  
    - Generate a new random Minecraft food item.  

- Update the display:  
  - Render Creeper snake segments, Minecraft food items, and the themed background.  
  - Show the score using a Minecraft font style.  

- Add a delay to regulate the snake's movement speed.  

## End Game

- Display a "Game Over" screen styled like Minecraft’s "You Died" message.  
- Show the final score and provide options to "Play Again?" or "Exit".  
