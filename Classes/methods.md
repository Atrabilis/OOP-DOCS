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
 
## Methods vs. Functions

A function is a reusable block of code that performs a specific task. A method, while essentially the same, is tied to a class and has access to the properties of the object it belongs to.

A method automatically receives the object it is called on as its first parameter (`self`):

```python
class Soldier:
    health = 100

    def take_damage(self, damage, multiplier):
        # "self" refers to the instance invoking the method
        damage *= multiplier
        self.health -= damage


dalinar = Soldier()
# "damage" and "multiplier" are explicitly passed as arguments
# "dalinar" is implicitly passed as the first argument, "self"
dalinar.take_damage(20, 2)
print(dalinar.health)  # 60

adolin = Soldier()
adolin.take_damage(10, 3)
print(adolin.health)   # 70
```

A method can modify the internal state of the object, so it may not always return a value. Instead, it might directly alter the object's properties.

## The OOP Debate

While functions tend to be more explicit, some developers argue that functional programming is superior to object-oriented programming. However, neither paradigm is objectively better. The most effective developers are proficient in both approaches and apply them as needed.

- **Functions (FP):** More explicit, with data and logic typically separated.  
- **Methods (OOP):** More implicit, combining data and behavior, which can lead to a more organized codebase.

Ultimately, the decision between paradigms is about balancing their respective strengths and weaknesses.

