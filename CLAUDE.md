# Dragon Flight Game - Project Summary

## Game Overview
A web-based side-scrolling flight game for a 5-year-old, inspired by Flappy Bird mechanics but more forgiving. Built with Phaser 3 framework.

## Current Implementation

### Core Mechanics
- Dragon constantly flies right (auto-scroll)
- SPACE or UP ARROW = Flap wings (upward velocity boost)
- DOWN ARROW = Duck (faster downward movement, wings fold)
- P = Pause/Resume
- Gravity constantly pulls dragon down
- 5 health hearts (lose 1 per obstacle hit, gain 1 per star collected)
- Score increases as obstacles pass and stars are collected
- Progressive difficulty - speed increases every 100 points

### Visual Design
- **Hand-drawn aesthetic using Rough.js library**
- Detailed green dragon with sketchy, organic lines:
  - Separate body, wings, head, tail, horns, spikes
  - Animated wings (flap on key press, idle gentle wave motion)
  - Body tilts up when flapping, down when ducking
  - Wings fold when ducking
  - Eye with pupil and shine
  - Golden decorative elements with rough edges
- Random obstacles (rocks, stalactites) with hand-drawn textures
- Collectible golden stars with sketchy glow effect
- UI shows health hearts, score, level, pause hint

### Technical Details
- Single HTML file (Phaser 3.55.2 + Rough.js 4.5.2 from CDN)
- Dragon is a Phaser Container with Rough.js-generated textures
- Graphics drawn to offscreen canvas, converted to Phaser textures
- Physics: Arcade physics with gravity
- Obstacles/collectibles spawn at random Y positions, scroll left
- Roughness values: 1.5-2.5 for authentic sketchy feel
- Hachure and solid fill styles for texture variety
- No localStorage (not supported in Claude.ai artifacts)
- All game state in memory

## Known Issues/Limitations
- No fire breathing yet
- Obstacle variety is limited
- No level-specific designs (random generation only)
- Simple collision detection
- Restart requires page refresh

## Next Steps to Consider
1. Add fire breathing mechanic (another key)
2. Replace graphics with actual sprite images/animations
3. Add sound effects
4. Create designed levels instead of random obstacles
5. Add proper restart button
6. More obstacle types and variety
7. Background scrolling/parallax
8. Power-ups beyond health stars

## File Structure
Currently: Single `dragon-game.html` file containing all HTML, CSS, JavaScript, and game logic.
