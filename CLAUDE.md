# Dragon Flight Game - Project Summary

## Game Overview
A web-based side-scrolling flight game for a 5-year-old, inspired by Flappy Bird mechanics but more forgiving. The dragon flies through a hand-drawn cave tunnel, avoiding obstacles and collecting stars. Built with Phaser 3 and Rough.js frameworks.

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
- **Mixed art style:**
  - Animated sprite-based dragon (cute cartoon style)
  - Hand-drawn cave environment using Rough.js library
- **Dragon:**
  - 6-frame sprite animation with wing flapping
  - Green body with orange wings and golden horns
  - Smooth frame-based animation (10 fps when flapping, 6 fps idle)
  - Body tilts up when flapping, down when ducking
  - Red tint applied when defeated
- **Scrolling cave tunnel environment:**
  - Rocky cave walls at top and bottom with irregular edges
  - Walls scroll horizontally creating sense of forward movement
  - Each wall segment has unique procedurally-generated texture
  - Hachure-filled textures for depth and hand-drawn feel
  - Creates confined tunnel preventing edge camping
  - Infinite tunnel effect with seamless segment wrapping
- Random obstacles (rocks, stalactites) with hand-drawn textures
- Collectible golden stars with sketchy glow effect
- UI shows health hearts, score, level, pause hint

### Technical Details
- Single HTML file (Phaser 3.55.2 + Rough.js 4.5.2 from CDN)
- Dragon: Animated sprite from dragon_sprites.png (6 frames, 100x100px each)
- Environment graphics drawn to offscreen canvas via Rough.js, converted to textures
- Physics: Arcade physics with reduced gravity (400) for easier control
- Scrolling cave walls with 3 segments each (top/bottom) for infinite tunnel
- Physics-based collision detection with cave walls (500ms damage cooldown)
- Walls scroll at same speed as obstacles for cohesive movement
- Obstacles 25% smaller and spawn 25% slower than original
- Obstacles/collectibles spawn at random Y positions, scroll left
- Roughness values: 1.5-2.5 for authentic sketchy feel
- Hachure and solid fill styles for texture variety
- Camera shake effect on wall impacts
- Game pauses until player presses SPACE to start
- No localStorage (not supported in Claude.ai artifacts)
- All game state in memory

## Known Issues/Limitations
- No fire breathing yet
- Obstacle variety is limited (only rocks and stalactites)
- Obstacles spawn randomly (no designed level patterns)
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
- `dragon-game.html` - Main game file with all HTML, CSS, JavaScript, and game logic
- `dragon_sprites.png` - Dragon sprite sheet (6 frames for wing animation)
- `CLAUDE.md` - This documentation file
