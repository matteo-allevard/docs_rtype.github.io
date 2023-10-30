# Graphics Class Documentation

The `Graphics` class is a C++ class that provides a graphical rendering system. It is used for rendering objects and handling user inputs. This documentation describes the class structure and its functions.

## Class Structure

The `Graphics` class is structured as follows:

- `Drawable` class: A nested class used to represent drawable objects.
  - Properties:
    - `ID`: Unique identifier for the drawable.
    - `xPos`, `yPos`: Position of the drawable.
    - `spriteConstructor`: A pointer to a `SpriteConstruction` object for creating the sprite.
    - `texture`, `sprite`: Objects for texture and sprite rendering.
    - `animationState`: State of the animation.

- `Graphics` class: The main class responsible for rendering and handling user inputs.
  - Properties:
    - `window`: A shared pointer to the rendering window.
    - `event`: Event handler.
    - `drawables`: Vector of shared pointers to `Drawable` objects.
    - `spriteConstructors`: Vector of `SpriteConstruction` objects for sprite initialization.

    [*spriteConstructors documentation*](./spriteConstructors.md)

## Public Methods

### Constructor and Destructor

- `Graphics()`: Constructor for the `Graphics` class.
- `~Graphics()`: Destructor for the `Graphics` class.

### Initialization

- `void build(unsigned int width, unsigned int height, unsigned int frameRateLimit, const std::vector<SpriteConstruction> &spriteInits)`: Initialize the graphics system with window dimensions and frame rate limit.
- `void createDrawable(int ID, int objectID, float x = 0.0, float y = 0.0, int rectState = -1)`: Create a drawable object with the specified properties.

### Input Handling

- `std::vector<std::pair<int, int>> getInputs()`: Get user inputs as pairs of input type and status.

### Position and Size Information

- `float getXPositionByID(int ID)`: Get the X position of a drawable object by its ID.
- `float getYPositionByID(int ID)`: Get the Y position of a drawable object by its ID.
- `void setPositionByID(int ID, float x, float y)`: Set the position of a drawable object by its ID.
- `float getSpriteWidthByID(int ID)`: Get the width of a drawable object's sprite by its ID.
- `float getSpriteHeightByID(int ID)`: Get the height of a drawable object's sprite by its ID.

### Screen Dimensions

- `unsigned int getScreenWidth()`: Get the width of the rendering window.
- `unsigned int getScreenHeight()`: Get the height of the rendering window.

### Rendering

- `void clear()`: Clear the rendering window.
- `void display()`: Display the rendering window.
- `void draw()`: Draw all drawable objects on the window.

## Enumerations

The `Graphics` class includes the following enumerations for inputs and key statuses:

- `Inputs`: Defines various input types (e.g., UP, RIGHT, SPACE).
- `KeyStatus`: Defines key statuses (e.g., PRESSED, RELEASED).

These enumerations are used for handling user inputs.

The `Graphics` class provides a comprehensive graphics system for rendering objects and handling user interactions.

[return to README](../README.md)