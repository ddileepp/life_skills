# SOLID Principles Refactoring Report

## Scenario Overview

I recently joined a new software project where the existing codebase was difficult to understand and maintain. The code had tightly coupled classes and mixed responsibilities. Even small changes caused issues in multiple places. To improve maintainability and scalability, my team lead asked me to study the SOLID principles and refactor the codebase. SOLID helps in designing clean, flexible, and testable object-oriented software.

## What is SOLID

SOLID represents five object-oriented design principles:

* Single Responsibility Principle
* Open Closed Principle
* Liskov Substitution Principle
* Interface Segregation Principle
* Dependency Inversion Principle

## Single Responsibility Principle (SRP)

A class should have only one reason to change.

### Example

~~~
class UserManager {
  createUser(user) {
    console.log("User created:", user);
  }
}

class EmailService {
  sendEmail(user) {
    console.log("Email sent to:", user);
  }
}
~~~

## Open Closed Principle (OCP)

Software entities should be open for extension but closed for modification.

### Example

~~~
class Discount {
  calculate(price) {
    return price;
  }
}

class RegularDiscount extends Discount {
  calculate(price) {
    return price * 0.9;
  }
}

class FestivalDiscount extends Discount {
  calculate(price) {
    return price * 0.8;
  }
}
~~~

## Liskov Substitution Principle (LSP)

Subclasses should be replaceable for their base classes without breaking functionality.

### Example

~~~
class Bird {
  fly() {
    console.log("Bird is flying");
  }
}

class Sparrow extends Bird {
  fly() {
    console.log("Sparrow is flying");
  }
}
~~~

## Interface Segregation Principle (ISP)

Clients should not be forced to depend on methods they do not use.

### Example

~~~
class Printer {
  print() {
    console.log("Printing document");
  }
}

class Scanner {
  scan() {
    console.log("Scanning document");
  }
}
~~~

## Dependency Inversion Principle (DIP)

High-level modules should depend on abstractions, not concrete implementations.

### Example

~~~
class Database {
  connect() {}
}

class MySQLDatabase extends Database {
  connect() {
    console.log("Connected to MySQL Database");
  }
}

class UserService {
  constructor(database) {
    this.database = database;
  }

  connectDatabase() {
    this.database.connect();
  }
}
~~~

## Conclusion

Applying SOLID principles improves code readability, reduces coupling, and makes applications easier to maintain and extend. These principles are essential for building scalable and reliable software systems.

## References

* https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design
* https://www.youtube.com/playlist?list=PL6n9fhu94yhXjG1w2blMXUzyDrZ_eyOme
* https://guides.github.com/features/mastering-markdown/
