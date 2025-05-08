## Using a Constructor for Class Initialization

In practice, it's rare to see a class that defines properties directly as follows:

```python
class Soldier:
    name = "Legolas"
    armor = 2
    num_weapons = 2
```

A constructor is generally a better approach. It's a specific method within a class called `__init__`, which is automatically invoked when a new instance of the class is created.

Using a constructor, the code above would be refactored as follows:

```python
class Soldier:
    def __init__(self):
        self.name = "Legolas"
        self.armor = 2
        self.num_weapons = 2
```

This approach is not only safer (we'll discuss why later), but it also allows the initial values of the class properties to be configurable:

```python
class Soldier:
    def __init__(self, name, armor, num_weapons):
        self.name = name
        self.armor = armor
        self.num_weapons = num_weapons

soldier_one = Soldier("Legolas", 5, 10)
print(soldier_one.name)
# prints "Legolas"
print(soldier_one.armor)
# prints "5"
print(soldier_one.num_weapons)
# prints "10"

soldier_two = Soldier("Gimli", 2, 1)
print(soldier_two.name)
# prints "Gimli"
print(soldier_two.armor)
# prints "2"
print(soldier_two.num_weapons)
# prints "1"
```

This method of initialization provides flexibility and ensures that each instance can have distinct values for its properties, making the class more versatile and secure.
