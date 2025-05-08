## Classes

A **class** is a blueprint for creating custom types in an object-oriented language like Python. It defines attributes and behaviors for its instances.

    class Soldier:
        def __init__(self, health=5, armor=3, damage=2):
            self.health = health
            self.armor = armor
            self.damage = damage

- A class is a type, like `int` or `str`, but defined by the user.  
- The `__init__` method initializes each new object’s state.

---

## Objects (Instances)

An **object** is a specific **instance** of a class. It follows the structure of its class but holds its own attribute values.

    # Instances of the Soldier class
    aragorn = Soldier(health=50)  # health = 50, armor = 3, damage = 2
    boromir = Soldier()           # health = 5,  armor = 3, damage = 2

    print(aragorn.health)  # 50
    print(boromir.health)  # 5

- Each object maintains its own state (O(k) space per object, where k = number of attributes).

---

## Another Example: Archer

    class Archer:
        def __init__(self, health=40, arrows=10):
            self.health = health
            self.arrows = arrows

    # Create instances of the Archer class
    legolas = Archer()          # health = 40, arrows = 10
    bard    = Archer(arrows=15) # health = 40, arrows = 15

    print(legolas.arrows)  # 10
    print(bard.arrows)     # 15

- Objects `legolas` and `bard` share the same class structure but have independent attribute values.  
- Constructors (`__init__`) allow setting defaults and overrides for each instance.
