# Side-Scroller Survival Game

**A 2D side-scrolling survival shooter built from scratch with vanilla JavaScript, the HTML5 Canvas API and CSS — no game engine.**

### ▶ [Play it in your browser](https://monicadfm.github.io/Sidescroller-Game-Code/)

Survive as long as you can while waves of slimes chase you across a scrolling world. Shoot them for points, dash out of trouble and don't fall off the left edge of the screen.

---

## Controls

| Key | Action |
| --- | --- |
| `A` / `D` | Move left / right |
| `W` | Jump |
| `Space` | Dash |
| `U` | Shoot |

## Features

- **Game loop** running at 60 fps with `requestAnimationFrame`
- **Five-layer parallax background** that scrolls continuously and pushes the player back
- **Player movement** with gravity, jumping, a dash ability and directional shooting with a fire-rate cooldown
- **Five enemy types** (slimes) with different speed, health and point values, spawned in randomised waves that chase the player
- **Collision detection** for player–enemy and projectile–enemy hits
- **Health system** with hearts and temporary invincibility after taking damage
- **Live score** and a game-over message showing the final score, then back to the menu
- **Character-selection menu** (the Ranger is currently playable)

## Tech

- JavaScript (ES6 modules and classes)
- HTML5 Canvas API
- CSS
- Deployed with GitHub Pages

## Code structure

```
index.html            Entry point (redirects to the menu)
Menu/                 Character-selection screen (HTML, CSS, JS)
Game/
  main.js             Input handling and the main game loop
  Player.js           Movement, jumping, dashing, shooting, health
  Enemy.js            Enemy behaviour (chasing, damage)
  enemyController.js  Spawning enemy types, hit detection, scoring
  bullet.js           Projectile
  bulletcontroller.js Projectile management and clean-up
  background.js       Parallax background layers
Background/           Background layer images
PlayerImgs/           Character sprites
```

## Running locally

No build step is needed. Because the game uses ES6 modules, serve the folder with any static server instead of opening the file directly, for example:

```bash
npx serve .
# or
python -m http.server
```

Then open `http://localhost:3000` (or `:8000`) in your browser.

## Author

**Mónica Moura** — [GitHub](https://github.com/monicadfm) · [Portfolio](https://monicadfm.github.io/Portfolio/)
