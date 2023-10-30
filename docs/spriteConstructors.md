# SpriteConstruction Class Documentation

The `SpriteConstruction` class is a C++ class used for constructing and configuring sprites for rendering. It defines the structure of sprite objects and their properties. This documentation describes the class structure and its functions.

## Class Structure

The `SpriteConstruction` class is structured as follows:

- `spriteRect` structure: A structure representing a rectangle for sprite rendering. It includes properties for the left, top, width, and height of the rectangle.

- `SpriteConstruction` class: The main class responsible for defining sprite properties and animation.
  - Properties:
    - `ID`: Unique identifier for the sprite construction.
    - `xScale`, `yScale`: Scaling factors for the sprite.
    - `filePath`: Path to the sprite image file.
    - `animationRects`: A vector of `spriteRect` structures defining animation frames.

## Public Methods

### Constructor and Destructor

- `SpriteConstruction(int ID, const std::string &filePath, float xScale, float yScale)`: Constructor for the `SpriteConstruction` class. Initializes the sprite construction with an ID, file path, and scaling factors.
- `~SpriteConstruction()`: Destructor for the `SpriteConstruction` class.

### Adding Animation Frames

- `void addSpriteRect(int left, int top, int width, int height)`: Add a sprite rectangle for defining an animation frame. Parameters include the position and dimensions of the frame.

## Properties

- `ID`: Unique identifier for the sprite construction.
- `xScale`, `yScale`: Scaling factors for the sprite.
- `filePath`: Path to the sprite image file.
- `animationRects`: A vector of `spriteRect` structures, each defining an animation frame.

## Example Usage

Here's an example of how to use the `SpriteConstruction` class:

```cpp
SpriteConstruction sprite(1, "sprites/player.png", 1.0, 1.0);
sprite.addSpriteRect(0, 0, 32, 32);  // Define the first animation frame.
sprite.addSpriteRect(32, 0, 32, 32); // Define the second animation frame.
```


[return to GUI DOC](./gui.md)


[return to README](../README.md)