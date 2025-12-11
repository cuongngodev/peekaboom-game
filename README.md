# 🎮 PeeKaBoom Game

A fun, interactive browser-based game inspired by the "Red Light, Green Light" concept from Squid Game. Players race to the finish line while avoiding being caught moving when Pikachu is watching!

![PeeKaBoom Logo](logo/peekaboom_logo.jpg)

## 📖 Table of Contents

- [Overview](#overview)
- [Game Gallery](#game-gallery)
- [Features](#features)
- [Game Rules](#game-rules)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [How to Play](#how-to-play)
- [Game Mechanics](#game-mechanics)
- [Customization](#customization)
- [Room for Improvement](#room-for-improvement)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)

## 🎯 Overview

PeeKaBoom is a multiplayer racing game where players must move their characters to the finish line without being caught by the watchful eyes of Pikachu. The game combines character customization, timing-based gameplay, and competitive racing mechanics to create an engaging experience.

## 🖼️ Game Gallery

### Squid Game Characters
Meet the characters from the hit series Squid Game that you can play as:

<table>
  <tr>
    <td align="center">
      <img src="public/seong-gi-hun.png" width="150" alt="Seong Gi-hun"/><br/>
      <b>Seong Gi-hun</b><br/>
      Player 456
    </td>
    <td align="center">
      <img src="public/cho-sang-woo.png" width="150" alt="Cho Sang-woo"/><br/>
      <b>Cho Sang-woo</b><br/>
      Player 218
    </td>
    <td align="center">
      <img src="public/kang-sae-byeok.png" width="150" alt="Kang Sae-byeok"/><br/>
      <b>Kang Sae-byeok</b><br/>
      Player 067
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="public/oh-il-nam.png" width="150" alt="Oh Il-nam"/><br/>
      <b>Oh Il-nam</b><br/>
      Player 001
    </td>
    <td align="center">
      <img src="public/jang-deok-su.png" width="150" alt="Jang Deok-su"/><br/>
      <b>Jang Deok-su</b><br/>
      Player 101
    </td>
  </tr>
</table>

### The Watcher
The game's referee - Pikachu watches over the race and catches players who move at the wrong time!

<table>
  <tr>
    <td align="center">
      <img src="watcher/pikachu/pikachu-watch.png" width="200" alt="Pikachu Watching"/><br/>
      <b>Pikachu - Watching</b><br/>
      Don't move! 👀
    </td>
    <td align="center">
      <img src="watcher/pikachu/pikachu-dont-watch.png" width="200" alt="Pikachu Not Watching"/><br/>
      <b>Pikachu - Not Watching</b><br/>
      Move now! 🏃
    </td>
  </tr>
</table>

### Pokemon Characters
Choose from powerful Pokemon characters (fetched dynamically from PokeAPI):
- 🔥 **Charizard** - The fire-flying dragon
- 🐉 **Dragonite** - The powerful dragon type
- 🦊 **Eevee** - The evolution Pokemon
- 🌊 **Gyarados** - The intimidating sea serpent

## ✨ Features

### Character Selection
- **Two Character Types**:
  - **Squid Game Characters**: Seong Gi-hun, Cho Sang-woo, Kang Sae-byeok, Oh Il-nam, Jang Deok-su
  - **Pokemon Characters**: Charizard, Dragonite, Eevee, Gyarados
- **Custom Skin Colors**: Choose from 5 different color skins for your character
- **Dual Player Support**: Play with 1 or 2 players

### Gameplay Features
- **Two Difficulty Levels**:
  - Easy Mode: 20 seconds time limit
  - Hard Mode: 15 seconds time limit
- **Dynamic Pikachu Watcher**: Randomly switches between watching and not watching states
- **Keyboard Controls**:
  - Player 1: Right Arrow Key (→)
  - Player 2: D Key
- **Real-time Timer**: Countdown timer based on selected difficulty
- **Win/Lose Conditions**: First to finish line wins, getting caught moving results in game over

### User Interface
- Player registration form with validation
- Character selection screen
- Skin color customization
- Live game status updates
- Responsive game controls
- Play again functionality

## 🎲 Game Rules

1. **Registration**: Enter player names and ages (must be between 10-99 years old)
2. **Character Selection**: Each player chooses a character from Squid Game or Pokemon
3. **Skin Selection**: Customize character appearance with color skins
4. **Difficulty Selection**: Choose Easy (20s) or Hard (15s) mode
5. **Movement**: 
   - Move ONLY when Pikachu is NOT watching
   - Stop immediately when Pikachu turns to watch
6. **Winning**: First player to reach the finish line wins
7. **Losing**: Getting caught moving while Pikachu watches results in elimination

## 💻 Technologies Used

- **HTML5**: Structure and markup
- **CSS3**: Styling and animations
- **JavaScript (ES6+)**: Game logic and interactivity
- **jQuery 3.7.1**: DOM manipulation and event handling
- **PokeAPI**: Fetching Pokemon character images
- **LocalStorage**: Saving game state and player data

## 📁 Project Structure
## 🎮 How to Play

### Step 1: Player Registration
1. Enter Player 1's name and age
2. (Optional) Click "Add/Remove Player 2" to toggle second player
3. Enter Player 2's information if playing with two players
4. Click "Start Game" to proceed

### Step 2: Character Selection
1. Player 1 selects a character (Squid Game or Pokemon)
2. Player 1 chooses a skin color
3. Click "Select" to confirm
4. Player 2 repeats the process
5. Click "Play" when both players are ready

### Step 3: Gameplay
1. Select difficulty (Easy or Hard)
2. Watch Pikachu carefully!
3. Move forward when Pikachu is NOT watching
4. STOP immediately when Pikachu turns to watch
5. Race to the finish line before time runs out

### Controls
- **Player 1**: Press and hold the **Right Arrow Key (→)** to move
- **Player 2**: Press and hold the **D Key** to move

## ⚙️ Game Mechanics

### Player Movement
- Players can only move when `isPikachuWatching = false`
- Movement speed: 2% per frame (50ms intervals)
- Players must reach 95% position to win (finish line)

### Pikachu Watch Cycle
- Randomly switches between watching/not watching
- Interval: 1-3 seconds (randomized)
- Movement detection occurs 5ms after Pikachu starts watching
- Visual and text feedback for current state

### Timer System
- Easy Mode: 20 seconds
- Hard Mode: 15 seconds
- Game ends when timer reaches 0
- Timer updates every second

### Win/Lose Conditions
- **Win**: First player to reach finish line (95% position)
- **Lose**: 
  - Caught moving while Pikachu is watching
  - Timer runs out before reaching finish line

## 🎨 Customization

### Adding New Characters

#### Squid Game Characters
Edit `package.json/squid-game-characters.json`:
```json
{
  "id": 6,
  "name": "Character Name",
  "koreanName": "Korean Name",
  "playerNumber": "XXX",
  "imageUrl": "/public/character-image.png"
}
```

#### Pokemon Characters
Edit `CONFIG.POKEMON_NAMES` in `scripts/characters.js`:
```javascript
POKEMON_NAMES: ['Charizard', 'Dragonite', 'Eevee', 'Gyarados', 'NewPokemon']
```

### Changing Skin Colors
Modify `CONFIG.SKIN_COLORS` in `scripts/characters.js`:
```javascript
SKIN_COLORS: ['#fff632', '#ffe6e2', '#ff9808', '#fd1124', '#12deed', '#YourColor']
```

### Adjusting Game Difficulty
Modify time limits in `scripts/gameplay.js`:
```javascript
function setDifficulty(level) {
    timeLimit = level === 'easy' ? 20 : 15; // Change values here
}
```

## � Room for Improvement

This project has several areas that could benefit from refactoring and enhancement to improve code quality, maintainability, and user experience.

### 🏗️ Code Architecture & Design Patterns

#### 1. **Separate Concerns with Class-Based Architecture**
Currently, the code uses procedural programming with global variables and functions scattered throughout. Consider refactoring to use classes:

#### 2. **Implement MVC/MVP Pattern**
- **Model**: Game state, player data, character data
- **View**: DOM manipulation and rendering
- **Controller**: Game logic and user input handling

### 🔊 Audio System

#### Add Sound Effects & Music

**Needed Audio Files:**
- Background music (looping)
- Footstep/movement sounds
- Pikachu watching alert sound
- Victory fanfare
- Defeat sound
- Button click sounds
- Character selection sound
## 👨‍💻 Author

**cuongngodev**
- GitHub: [@cuongngodev](https://github.com/cuongngodev)

## 🙏 Acknowledgments

- Squid Game for character inspiration
- [PokeAPI](https://pokeapi.co/) for Pokemon data and images
---

**Enjoy the game 🎮🏆**