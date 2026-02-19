# SOLID Principles – Refactoring Experience Report

## Project Background

When I joined this project, the codebase was difficult to understand and maintain. Many classes were handling multiple responsibilities, and small changes were affecting different parts of the system. It was hard to debug issues and risky to add new features.

To improve the structure and maintainability of the application, I studied the SOLID principles and refactored the code accordingly. After applying these principles, the code became cleaner, more modular, and easier to extend.

---

## What is SOLID?

SOLID is a set of five object-oriented design principles that help developers write clean, scalable, and maintainable software.

It stands for:

- Single Responsibility Principle  
- Open Closed Principle  
- Liskov Substitution Principle  
- Interface Segregation Principle  
- Dependency Inversion Principle  

---

## 1 Single Responsibility Principle (SRP)

A class should have only one responsibility or purpose.

Earlier, some classes were doing multiple tasks at once, which made them hard to maintain. After refactoring, each class now focuses on one specific task. This makes the system easier to test and modify.

---

## 2 Open Closed Principle (OCP)

Software components should be open for extension but closed for modification.

Instead of changing existing code whenever a new feature is needed, we extend the functionality by adding new components. This reduces the risk of breaking existing features.

---

## 3 Liskov Substitution Principle (LSP)

Subclasses should behave in a way that does not break the expectations of the base class.

In simple words, if we replace a parent class with its child class, the program should still work correctly without unexpected behavior.

---

## 4 Interface Segregation Principle (ISP)

Classes should not be forced to depend on methods they do not use.

Instead of creating large, complex classes, responsibilities are divided into smaller and more specific components. This keeps the design simple and focused.

---

## 5 Dependency Inversion Principle (DIP)

High-level modules should depend on abstractions, not concrete implementations.

Instead of tightly connecting one part of the system to a specific implementation (like a specific database), we design the system in a flexible way so that components can be changed without affecting the overall structure.

---

## What I Learned

Applying SOLID principles helped me:

- Improve code readability  
- Reduce tight coupling  
- Make the application easierto extend  
- Write cleaner and more maintainable code  
- Think more clearly about system design  

---

## Conclusion

Refactoring the project using SOLID principles significantly improved the structure and maintainability of the codebase. I now understand the importance of designing software thoughtfully instead of just making it work.

These principles will help me build scalable and reliable applications in the future.
