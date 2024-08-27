# Simon-Game
---
### Description:
This is a simple Simon memory game implemented using JavaScript, HTML, and CSS. The game randomly generates a sequence of button flashes, and the player has to replicate the sequence by clicking the buttons in the correct order. Each successful level adds another step to the sequence, and the player must continue matching the sequence to progress. If the player makes a mistake, the game ends, and the score (level) is displayed.

### How to Play:
1. Press any key on the keyboard to start the game.
2. Watch the sequence of button flashes carefully.
3. Click the buttons in the exact order the sequence was shown.
4. If you correctly match the sequence, the game will proceed to the next level, where an additional button will be added to the sequence.
5. If you make a mistake, the game will end, and your score (level reached) will be displayed.
6. Press any key again to restart the game.

### Files:
- **index.html:** Contains the structure of the page with buttons representing different colors and a heading to display the current level or game status.
- **styles.css:** Provides the styles for the buttons, background, and animations for the button flashes.
- **script.js:** Contains the JavaScript logic for the game.

### JavaScript Code Overview:
- `gameSeq` and `userSeq`: Arrays that store the sequence generated by the game and the sequence of buttons clicked by the user.
- `btns`: An array of color strings that correspond to the button classes.
- `started`: A flag to check whether the game has started.
- `h2`: A reference to the level display element in the HTML.
- `level`: Tracks the player's current level.

### Key Functions:
1. **`btnFlash(btn)`**: Adds a flashing effect to the game-generated button and removes it after a short delay.
2. **`userFlash(btn)`**: Adds a flashing effect when the user presses a button and removes it after a short delay.
3. **`levelUp()`**: Advances the level by adding a new random button to the sequence and flashing that button.
4. **`check(idx)`**: Checks if the user's input matches the game sequence at the given index. If the entire sequence is correct, the game proceeds to the next level. If there's a mistake, the game displays "Game Over" and allows restarting.
5. **`btnPress()`**: Handles the button click event, flashes the button, adds it to `userSeq`, and calls the `check()` function to validate the user's input.
6. **`reset()`**: Resets the game variables when the game is over, allowing the player to start again.

### Notes:
- The buttons are selected based on their respective color IDs in the HTML.
- The game uses animations for flashing buttons to give visual feedback to the player.
- The game detects incorrect sequences and ends when the player makes a mistake, showing the score before resetting.

---
