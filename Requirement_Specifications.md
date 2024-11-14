# Requirements Specification: Snake

**Game Name**: Snake  
**Team Members**: Jonathan and Lucas  
**Client**: Kennedy  
**Date**: 11/14/2024

---

## Game Overview

- **Brief Description**:  
  Snake is a classic arcade-style game where the player controls a snake that grows longer each time it eats food. The player must avoid crashing into the walls or the snake’s own body. The game features a pixelated art style inspired by the game "Minecraft."

- **Objective**:  
  The goal of the game is to make the snake grow bigger by eating food without hitting the wall or hitting itself.

---

## Functional Requirements

- **Core Features**:  
  - Track the snake's length and points based on how much food it eats.
  - Display the current score and high score.
  - Game over condition if the snake collides with the wall or itself.
  - Ability to restart the game after it ends.

- **User Interactions**:  
  - The player interacts with the game using the arrow keys to control the snake's movement.
  - The snake moves continuously in the direction specified by the player until another direction is chosen.

---

## Non-Functional Requirements

- **Usability**:  
  - The game should be designed for ease of play with simple controls (arrow keys) to move the snake around, find food, and avoid obstacles (wall and body).
  - The user interface should be simple and intuitive, displaying the current score and high score clearly.

- **Performance**:  
  - The game should perform smoothly with a stable frame rate (FPS). There should be no lag or stuttering in the movement of the snake or food.

- **Cross-Platform Compatibility**:  
  - The game should work on multiple devices, including PC, phones, and other devices that support web-based games.

---

## Design Requirements

- **Graphics and Visuals**:  
  - The game's graphics should have a **pixelated** style, drawing inspiration from the **Minecraft** aesthetic (blocky design, simple textures, etc.).
  - The snake and food should be clearly distinguishable with pixel-based art.

- **Audio**:  
  - Sound effects should be simple and playful. A "burp" sound will play whenever the snake eats food to enhance the satisfaction of the action.

---

## Data Requirements

- **Data to be Saved or Tracked**:  
  - The game should track the **current score** and **high score**.
  
- **How Data Will Be Stored**:  
  - The data (score and high score) will be stored **locally on the device**. This could be done using browser storage (localStorage for web versions) or local storage on mobile devices.

---

## Collaboration with Client

- **How will you gather feedback from the client in each sprint?**  
  - Feedback will be gathered through **forms or surveys** at the end of each sprint. This will help understand what works, what needs to be improved, and whether the game is heading in the right direction.

- **How will you ensure the game is developing according to the client's needs?**  
  - By **establishing clear goals** and **requirements** at the beginning of the project, and regularly gathering feedback throughout the development process to make necessary adjustments. This iterative approach ensures the game evolves according to the client’s vision.

