# `registry` Class Functions

The `registry` class provides various functions for managing components and entities in a game or application. Below are the details of these functions:

## Constructor and Destructor

### `registry()`

The constructor for the `registry` class.

### `~registry()`

The destructor for the `registry` class.

## Component Management

### `template <class Component> sparse_array<Component> &register_component()`

Create a container for a specific component type (`Component`). For example, you can register a component using `register_component<position_t>()`.

### `template <class Component> sparse_array<Component> &get_components()`

Get a reference to the container holding components of a specific type (`Component`).

### `template <class Component> const sparse_array<Component> &get_components() const`

Get a constant reference to the container holding components of a specific type (`Component`).

### `template <typename Component> Component &add_component(const entity_t& to, Component&& c)`

Add a component of type `Component` to an entity specified by `to`.

### `template <typename Component> Component &set_component(const entity_t& to, Component&& c)`

Initialize a component for an entity specified by `to`.

### `template <typename Component> Component &get_component(const entity_t& to)`

Get a reference to the component of type `Component` for the specified entity.

## Entity Management

### `entity_t spawn_entity()`

Create a new entity and return its entity ID.

### `void kill_entity(const entity_t &entityID)`

Delete an entity with the specified entity ID.

### `bool isEntityValid(entity_t pos)`

Check if an entity with the given entity ID is valid (i.e., still exists).

These functions allow you to manage components and entities efficiently within your application.


[return to README](../README.md)
