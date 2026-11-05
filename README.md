# Asteroids

A small Asteroids-style arcade game built with Python and Pygame. Pilot the
ship, avoid incoming asteroids, and destroy them with your cannon.

## Requirements

- Python 3.13 or newer
- [Pygame](https://www.pygame.org/) 2.6.1
- [uv](https://docs.astral.sh/uv/) (recommended)

## Setup

Clone the repository and install the locked dependencies:

```bash
uv sync
```

## Run the game

```bash
uv run main.py
```

The game opens a 1280 × 720 window. Close the window to exit.

## Controls

| Key | Action |
| --- | --- |
| `W` | Move forward |
| `S` | Move backward |
| `A` | Rotate left |
| `D` | Rotate right |
| `Space` | Fire |

The ship’s direction is shown by the pointed end of the triangle. Hold
`Space` to fire repeatedly.

## Gameplay

Asteroids enter the play area from each edge and move toward the field. A
bullet destroys an asteroid on contact. Larger asteroids split into two
smaller, faster asteroids; the smallest asteroids disappear when destroyed.
The game ends when an asteroid collides with the player.

## Development

Compile the game modules without starting the window:

```bash
uv run python -m compileall -q main.py player.py shot.py asteroid.py asteroidfield.py circleshape.py
```
