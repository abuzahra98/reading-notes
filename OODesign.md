# SOLID OO Design

### Five Principles of Object-Oriented Programming

- `S`ingle-responsibility principle
  - "A class should have one and only one reason to change, meaning that a class should have only one job."
  - Having a class perform a single task makes each class an individual part of a greater machine, that can be disassembled, diagnosed and fixed or modified easily, rather than having a single large class full of interdependent methods that all collapse with one thing out of place.
- `O`pen-closed principle
  - "Objects or entities should be open for extension but closed for modification."
  - Rather than modifying existing, and perfectly functional code it is better to create a new class and inherit from the old one and overriding or extending behaviors
- `L`iskov-substitution principle
  - "Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T."
  - Child classes should perform the features of the Parent
- `I`nterface segregation principle
  - "A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use."
  - Like classes being broken up so that they each perform small, specific tasks well so too should interfaces be split apart for the same reasons
- `D`ependency Inversion Principle
  - "Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions."
  - Code should be flexible and be able to properly process whatever is thrown at it to a certain degree. Why hard-code a method to process a specific input when it can be dynamic and respond to whatever input you want to give it?

[<== Back to Readme](README.md)