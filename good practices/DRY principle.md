## DRY – Don’t Repeat Yourself

The DRY principle dictates that **every piece of knowledge or logic** in a system should have a **single, unambiguous representation**. Avoid duplicating code because:

### Why duplicated code is problematic

- **Risk of inconsistency**  
  Changing logic in one place but forgetting another leads to subtle bugs.  
- **Increased maintenance cost**  
  You must update every copy whenever requirements change.  
- **Waste of effort**  
  Writing the same code repeatedly slows down development and increases cognitive load.

### Benefits of applying DRY

- **Single source of truth**  
  All behavior lives in one place, making it easier to audit and test.  
- **Fewer bugs**  
  Eliminating duplication reduces the surface for potential errors.  
- **Faster development**  
  Reusing abstractions accelerates feature implementation and refactoring.

### How to implement DRY in your code

1. **Identify common patterns**  
   Look for repeated logic, literal values or structures.  
2. **Abstract into functions or classes**  
   Encapsulate shared behavior behind a clear interface.  
3. **Leverage language features**  
   - **Higher-order functions** (e.g. `map`, `filter`)  
   - **Inheritance** or **composition** in OOP  
   - **Utility modules** or **libraries**  
4. **Maintain clear documentation**  
   Document abstractions so their purpose and usage remain obvious.

> “Every time you duplicate code, you create a new place to have a bug.”  
> — Derived from DRY principles
