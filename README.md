# Pixel RPG Demo

A simple pixel-art RPG demo written in C++ with [raylib](https://www.raylib.com/). It is a small game engine experiment with real-time rendering and basic RPG mechanics, such as characters, enemies and props.

This is a work in progress, built as a demonstration of RPG mechanics in a pixel-art world.

## Features

- Real-time rendering with raylib
- Character, enemy and prop classes sharing a common base (`BaseCharacter`)
- Retro pixel-art style

## Tech Stack

- C++
- [raylib](https://www.raylib.com/) (bundled in `include/` and `lib/`)
- Make

## Building

The included `Makefile` targets Windows and links against the bundled raylib library:

```bash
make
```

The build links with `-lopengl32 -lgdi32 -lwinmm`, so it requires a Windows toolchain such as MinGW-w64.

> **Known issues**
> - The Makefile refers to lowercase source names (for example `../character.cpp`) and parent-folder paths. These do not match the files in this repository, so the build needs adjusting before it will run.
> - There is no `CMakeLists.txt` yet, so CMake builds are not currently supported.

## Project Structure

```
├── classy.cpp          # Entry point
├── Character.h/.cpp    # Player character
├── BaseCharacter.h/.cpp
├── Enemy.h/.cpp        # Enemies
├── prop.h/.cpp         # Props (scenery and objects)
├── Makefile
├── include/            # raylib headers
├── lib/                # raylib library
├── characters/         # Character sprites
└── nature_tileset/     # Tileset for the environment
```

## Contributing

Feedback and contributions are welcome.
