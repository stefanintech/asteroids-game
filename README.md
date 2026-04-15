# Asteroids Game

A classic Asteroids clone built with Python and pygame. Shoot rocks. Don't get hit. Try not to blink.

## About

This project is a from-scratch implementation of the Asteroids arcade game. It uses pygame's sprite group system to manage game objects and features asteroid splitting, a shooting cooldown, and basic game state logging.

## Features

- Player ship with rotation and thrust movement
- Asteroids that split into smaller pieces when shot
- Shooting with a cooldown (0.3s between shots)
- Collision detection between player, asteroids, and shots
- Game state and event logging via a dedicated logger module
- 1280x720 resolution, locked at 60 FPS

## Project Structure

```
asteroids-game/
├── main.py           # Game loop and sprite group setup
├── player.py         # Player ship logic
├── asteroid.py       # Asteroid behavior and splitting
├── asteroidfield.py  # Asteroid spawner
├── shot.py           # Projectile logic
├── circleshape.py    # Base class for circular game objects
├── constants.py      # All tunable game values
├── logger.py         # State and event logging
└── pyproject.toml    # Project config and dependencies
```

## Requirements

- Python 3.13+
- [uv](https://docs.astral.sh/uv/) (recommended)

## Installation and Running

Clone the repo:

```bash
git clone https://github.com/stefanintech/asteroids-game.git
cd asteroids-game
```

Install dependencies and run with `uv`:

```bash
uv run main.py
```

Or install manually with pip:

```bash
pip install pygame==2.6.1
python main.py
```

## Controls

| Key | Action |
|-----|--------|
| W | Thrust forward |
| A | Rotate left |
| D | Rotate right |
| Space | Shoot |

## Configuration

All game constants live in `constants.py`. Tweak values there to adjust difficulty, speed, asteroid size, and more.

```python
PLAYER_SPEED = 200
PLAYER_SHOOT_COOLDOWN_SECONDS = 0.3
ASTEROID_SPAWN_RATE_SECONDS = 0.8
ASTEROID_KINDS = 3  # Controls how many times asteroids split
```

## Planned Enhancements

Things I want to add or improve on as the project evolves:

**Gameplay**
- Scoring system
- Multiple lives and respawning
- Screen wrapping so objects reappear on the opposite side instead of disappearing

**Player**
- Acceleration-based movement instead of instant velocity
- Triangular hitbox to match the ship's actual shape
- Shield power-up
- Speed power-up
- Droppable bombs

**Weapons**
- Multiple weapon types

**Visuals**
- Explosion effects when asteroids are destroyed
- Lumpy, irregular asteroid shapes instead of perfect circles
- Background image

## Built With

- [Python 3.13](https://www.python.org/)
- [pygame 2.6.1](https://www.pygame.org/)
- [uv](https://docs.astral.sh/uv/)
