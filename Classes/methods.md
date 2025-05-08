## Methods

Classes can define **methods**, which are functions bound to the class with access to its properties. Methods provide both structure and behavior:

    class Soldier:
        def __init__(self, health=5):
            self.health = health

        def take_damage(self, damage: int) -> None:
            """Reduce health by damage amount."""
            self.health -= damage

    # Usage examples
    soldier_one = Soldier()
    soldier_one.take_damage(2)
    print(soldier_one.health)  # 3

    soldier_two = Soldier()
    soldier_two.take_damage(1)
    print(soldier_two.health)  # 4

- Methods are defined inside the class. The first parameter, **self**, refers to the instance on which the method is called.
- Invoking `instance.method()` performs method lookup and call in **O(1)** time.
- Accessing attributes (e.g., `self.health`) is **O(1)** time and uses **O(1)** extra space per access.

---

### Benefits

- **Encapsulation**  
  Bundles data and behavior together, clarifying valid operations on the object.

- **Reusability**  
  Each method is stored once per class, regardless of how many instances exist.

- **Maintainability**  
  Changes to behavior occur in a single location, reducing the risk of inconsistencies.

---

### Complexity

- **Temporal**  
  - Defining a method: O(1) per method.  
  - Method call and attribute access: O(1).

- **Spatial**  
  - Each instance consumes O(k) space, where k = number of attributes.  
  - Methods consume O(1) space per class, shared by all instances.
