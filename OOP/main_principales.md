OOP to creating well-structured, reusable, maintainable, and extendable code. They help model real-world concepts effectively and solve complex problems by breaking them down into interacting objects.

Here are the main principales of OOP:

- **Inheritance** is a mechanism that allows a class (called a derived or subclass) to inherit properties (fields) and behaviors (methods) from another class (called a base or superclass). This enables the creation of a class hierarchy where a class can inherit characteristics from a parent class.
Inheritance promotes code reuse and the creation of specialized classes based on existing classes.

- **Abstraction** involves representing the essential characteristics of an object while hiding complex or unnecessary details. An abstract class is a class that cannot be instantiated directly but can serve as a blueprint for other classes.
Abstraction simplifies complexity by focusing on what is relevant to a particular problem.

- An **interface** is a contract that defines a set of methods that classes must implement. A class can implement multiple interfaces, ensuring that the class exhibits the behaviors specified by the interface.
Interfaces facilitate polymorphism (see below) by allowing multiple classes to respond to a common set of methods.

- **Polymorphism** means that objects of different classes can be treated uniformly if they share a common interface. There are two forms of polymorphism: static and dynamic.
Static polymorphism allows calling methods on an object without knowing its exact type at compile time, using interfaces or base classes.
Dynamic polymorphism allows invoking methods specific to the actual object at runtime, relying on inheritance and method overriding.
Encapsulation:

- **Encapsulation** involves grouping data (attributes) and methods (behaviors) that manipulate them into a single unit called a class. Access to the class's data is then controlled using access modifiers (such as public, private, protected).
Encapsulation protects object data from unauthorized modifications and promotes the principle of information hiding, where only necessary members of a class are exposed externally.
