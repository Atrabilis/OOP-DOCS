## Creating Instances of a Class

A class can be thought of as a "blueprint" or a "template" for creating objects. For example, I can create a `Wall` class like this:

```python
class Wall:
    def __init__(self, depth, height, width):
        self.depth = depth
        self.height = height
        self.width = width
```

With this `Wall` class, I can then create three different "instances" of the class. In other words, I can create three separate objects, each with its own set of properties, independent of one another:

```python
wall_maria = Wall(1, 2, 3)
wall_rose = Wall(4, 5, 6)
wall_sina = Wall(9, 8, 7)
```

Each of these instances (`wall_maria`, `wall_rose`, `wall_sina`) represents a unique object with its own values for the `depth`, `height`, and `width` properties.
