# Java Design Patterns — Comprehensive Reference Guide

> **Audience:** Experienced Java developers looking to strengthen their understanding of GoF design patterns.
> **Source:** [Java-Design-Pattern](https://github.com/mkejeiri/Java-Design-Pattern) repository — 29 pattern implementations with complete source code.
> **Based on:** *Design Patterns: Elements of Reusable Object-Oriented Software* (Gang of Four)

---

## Source Code Index

| # | Pattern | Category | Source |
|---|---------|----------|--------|
| 01 | Strategy (ScoreBoard) | Behavioral | [01_scoreBoard_strategy](01_scoreBoard_strategy/src/com/kejeiri) |
| 02 | Strategy (Payment) | Behavioral | [02_Strategy_Payment](02_Strategy_Payment/Payment/src/com/kejeiri/java/course) |
| 03 | Observer (Email/Pull) | Behavioral | [03_Observer_email](03_Observer_email/Observer/src/com/kejeiri/java/course) |
| 04 | Observer (Broadcast/Push) | Behavioral | [04_observerBroadcast](04_observerBroadcast/radioBroadcast/src/com/kejeiri/java/course) |
| 05 | Decorator | Structural | [05_icecreamdecoratorpattern](05_icecreamdecoratorpattern/decoratorpattern/src/com/kejeiri/java/course) |
| 06 | Simple Factory | Creational | [06_HamburgerFactoryPattern](06_HamburgerFactoryPattern/HamburgerFactoryPattern/src/com/kejeiri) |
| 07 | Factory Method | Creational | [07_HamburgerFactoryPattern_ENHANCED](07_HamburgerFactoryPattern_ENHANCED/HamburgerFactoryPattern/src/com/kejeiri) |
| 08 | Singleton (Lazy) | Creational | [08_Singleton_Lazily_Created](08_Singleton_Lazily_Created/SimpleDBConnector/src/com/java/course) |
| 09 | Singleton (Eager) | Creational | [09_Singleton_Eagerly_Created](09_Singleton_Eagerly_Created/SimpleDBConnector/src/com/java/course) |
| 10 | Singleton (DCL) | Creational | [10_Singleton_Lazily_Created_Double-check-locking](10_Singleton_Lazily_Created_Double-check-locking/SimpleDBConnector/src/com/java/course) |
| 11 | Command | Behavioral | [11_CommandPattern](11_CommandPattern/CommandPattern/src/com/java/course) |
| 12 | Adapter | Structural | [12_AdapterPattern](12_AdapterPattern/AdapterPattern/src/com/java/course) |
| 13 | Facade | Structural | [13_FacadePattern](13_FacadePattern/FacadePattern/src/com/java/course) |
| 14 | Template Method | Behavioral | [14_TemplatePattern](14_TemplatePattern/TemplatePattern/src/com/java/course) |
| 15 | Iterator | Behavioral | [15_IteratorPattern](15_IteratorPattern/IteratorPattern/src/com/java/course) |
| 16 | State (Anti-pattern) | Behavioral | [16_StatePattern](16_StatePattern/StatePattern/src/com/java/course) |
| 17 | State (OO Solution) | Behavioral | [17_StatePatternSolution](17_StatePatternSolution/StatePatternSolution/src/com/java/course) |
| 18 | Proxy | Structural | [18_ProxyPattern](18_ProxyPattern/ProxyPattern/src/com/java/course) |
| 19 | MVC | Architectural | [19_MVCDesignPattern](19_MVCDesignPattern/MVCDesignPattern/src/com/kejeiri/java/course) |
| 20 | Builder | Creational | [20_BuilderDesignPattern](20_BuilderDesignPattern/BuilderDesignPattern/src/com/kejeiri/java/course) |
| 21 | Builder (Interface) | Creational | [21_BuilderInterfaceDesignPattern](21_BuilderInterfaceDesignPattern/BuilderInterfaceDesignPattern/src/com/kejeiri/java/course) |
| 22 | Prototype | Creational | [22_PrototypeDesignPattern](22_PrototypeDesignPattern/PrototypeDesignPattern/src/com/java/course) |
| 23 | Mediator | Behavioral | [23_MediatorDesignPattern](23_MediatorDesignPattern/MediatorDesignPattern/src/com/java/course) |
| 24 | Visitor | Behavioral | [24_VisitorDesignPattern](24_VisitorDesignPattern/VisitorDesignPattern/src/com/kejeiri/java/course) |
| 25 | Memento | Behavioral | [25_MementoDesignPattern](25_MementoDesignPattern/MementoDesignPattern/src/com/java/course) |
| 26 | Interpreter | Behavioral | [26_InterpreterDesignPattern](26_InterpreterDesignPattern/InterpreterDesignPattern/src/com/java/course) |
| 27 | Chain of Responsibility | Behavioral | [27_ChainOfResponsabilityDesignPattern](27_ChainOfResponsabilityDesignPattern/ChainOfResponsabilityDesignPattern/src/com/java/course) |
| 28 | Bridge | Structural | [28_BridgeDesignPattern](28_BridgeDesignPattern/BridgeDesignPattern/src/com/java/course) |
| 29 | Flyweight | Structural | [29_FlyWeightDesignPattern](29_FlyWeightDesignPattern/FlyWeightDesignPattern/src/com/java/course) |

---

## Table of Contents

### Creational Patterns
1. [Singleton — Lazy Initialization (synchronized)](#singleton--lazy-initialization-synchronized)
2. [Singleton — Eager Initialization](#singleton--eager-initialization)
3. [Singleton — Double-Check Locking](#singleton--double-check-locking)
4. [Simple Factory — Hamburger](#simple-factory--hamburger)
5. [Factory Method — Enhanced Hamburger](#factory-method--enhanced-hamburger)
6. [Builder — User](#builder--user)
7. [Builder — (Variant 21)](#builder--variant-21)
8. [Prototype](#prototype)

### Structural Patterns
9. [Adapter](#adapter)
10. [Bridge](#bridge)
11. [Decorator](#decorator)
12. [Facade](#facade)
13. [Flyweight](#flyweight)
14. [Proxy](#proxy)

### Behavioral Patterns
15. [Strategy — ScoreBoard](#strategy--scoreboard)
16. [Strategy — Payment](#strategy--payment)
17. [Observer — Email (Pull Model)](#observer--email-pull-model)
18. [Observer — Broadcast (Push Model)](#observer--broadcast-push-model)
19. [Command](#command)
20. [Template Method](#template-method)
21. [Iterator](#iterator)
22. [State — Procedural (Anti-pattern)](#state--procedural-anti-pattern)
23. [State — Object-Oriented](#state--object-oriented)
24. [Mediator](#mediator)
25. [Visitor](#visitor)
26. [Memento](#memento)
27. [Interpreter](#interpreter)
28. [Chain of Responsibility](#chain-of-responsibility)

### Architectural Patterns
29. [MVC (Model-View-Controller)](#mvc-model-view-controller)

---

# Creational Patterns

Creational patterns deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.

---

## Singleton — Lazy Initialization (synchronized)

**GoF Category:** Creational

![Singleton Lazy](08_Singleton_Lazily_Created/SimpleDBConnector/figure1.jpg)

### Intent
Ensures a class has only one instance and provides a global point of access to it. The lazy variant delays creation until the instance is first needed, conserving resources when the object may never be used.

### When to Use
- Database connection pools where only one pool should exist
- Logger instances shared across the application
- Configuration managers that load settings once
- Thread pools, caches, dialog boxes, registry settings

### Key Participants
| Class | Role |
|-------|------|
| `DBConnector` | Singleton class with private constructor and static getInstance() |

### Complete Source Code

```java
package com.java.course;

public class DBConnector {
    // The single instance — initially null (lazy)
    private static DBConnector uniquedbcon;

    // Private constructor prevents external instantiation
    private DBConnector() { }

    // synchronized keyword: makes this method thread-safe
    // COST: Every call to getInstance() acquires a lock, even after instance exists
    public static synchronized DBConnector getInstance(){
        if (uniquedbcon == null){
            uniquedbcon = new DBConnector();
        }
        return uniquedbcon;
    }

    public void userConnect(){
        System.out.println("user is connected to db! : Object @ = " + uniquedbcon);
    }
}
```

```java
package com.java.course;

public class Main {
    public static void main(String[] args) {
        System.out.println("Creating a singleton connection to DB");
        DBConnector dbConnector = DBConnector.getInstance();
        dbConnector.userConnect();
    }
}
```

### How It Works — Step by Step
1. `DBConnector` declares a private static field `uniquedbcon` initialized to `null`
2. The constructor is `private` — no external code can call `new DBConnector()`
3. `getInstance()` is the only way to get the instance. It checks if `uniquedbcon` is null
4. If null, it creates the instance. If not, it returns the existing one
5. The `synchronized` keyword ensures only one thread can execute `getInstance()` at a time

### Pitfalls and Common Mistakes
- **Performance:** `synchronized` on the entire method means every call pays the lock cost, even when the instance already exists
- **Serialization:** If the class implements `Serializable`, deserialization creates a new instance. Override `readResolve()` to prevent this
- **Reflection:** Reflection can invoke the private constructor. Guard against it by throwing an exception in the constructor if an instance exists
- **Classloader issues:** Multiple classloaders can each load the Singleton class, creating multiple instances

### Connection to Other Patterns
- Often confused with **Static Utility Classes** — Singletons can implement interfaces and be polymorphic; static classes cannot
- Combined with **Factory** — a factory can be a singleton
- Combined with **Facade** — a facade is often implemented as a singleton

---

## Singleton — Eager Initialization

**GoF Category:** Creational

![Singleton Eager](09_Singleton_Eagerly_Created/SimpleDBConnector/figure1.jpg)

### Intent
Guarantees a single instance by creating it at class-loading time. Trades potential resource waste for simplicity and inherent thread safety without synchronization.

### When to Use
- When the singleton is always needed during application lifetime
- When construction is lightweight and fast
- When you want the simplest thread-safe implementation
- Application-wide configuration that's always accessed

### Key Participants
| Class | Role |
|-------|------|
| `DBConnector` | Singleton with instance created at class load |

### Complete Source Code

```java
package com.java.course;

public class DBConnector {
    // Instance created at class loading time — JVM guarantees thread safety here
    private static DBConnector uniquedbcon = new DBConnector();

    // Private constructor
    private DBConnector() { }

    // No synchronization needed — instance already exists
    public static DBConnector getInstance(){
        return uniquedbcon;
    }

    public void userConnect(){
        System.out.println("user is connected to db! : Object @ = " + uniquedbcon);
    }
}
```

```java
package com.java.course;

public class Main {
    public static void main(String[] args) {
        System.out.println("Creating a singleton connection to DB");
        DBConnector dbConnector = DBConnector.getInstance();
        dbConnector.userConnect();
    }
}
```

### How It Works — Step by Step
1. The static field is initialized with `new DBConnector()` at class loading time
2. The JVM guarantees that class initialization is thread-safe (happens-before relationship)
3. `getInstance()` simply returns the pre-created instance — no checks, no locks
4. The private constructor still prevents external instantiation

### Pitfalls and Common Mistakes
- **Resource waste:** If the instance is expensive to create and never used, resources are wasted
- **No exception handling:** If the constructor throws an exception, you get a `ExceptionInInitializerError` that's hard to debug
- **No lazy initialization:** Cannot pass parameters to the constructor at creation time since it's created before any client code runs

### Connection to Other Patterns
- Simpler alternative to **Double-Check Locking** when lazy initialization isn't required
- Can be combined with **Enum Singleton** (Joshua Bloch's recommended approach) for even better safety

---

## Singleton — Double-Check Locking

**GoF Category:** Creational

![Singleton DCL](10_Singleton_Lazily_Created_Double-check-locking/SimpleDBConnector/figure1.jpg)

### Intent
Achieves lazy initialization with minimal synchronization overhead. Only synchronizes during the first creation, then all subsequent calls are lock-free. The best-practice lazy singleton for performance-critical applications.

### When to Use
- When lazy initialization is required AND performance matters
- High-concurrency environments where lock contention is a concern
- When the singleton is expensive to create but may not always be needed

### Key Participants
| Class | Role |
|-------|------|
| `DBConnector` | Singleton using volatile + double-checked locking idiom |

### Complete Source Code

```java
package com.java.course;

public class DBConnector {
    private DBConnector() { }

    // volatile prevents instruction reordering during object construction
    // Without volatile, a thread could see a partially constructed object
    private volatile static DBConnector uniquedbcon;

    public static DBConnector getInstance(){
        // First check (no locking) — fast path for already-initialized case
        if (uniquedbcon == null) {
            // Only synchronize when instance might need creation
            synchronized ((DBConnector.class)) {
                // Second check (with lock held) — prevents duplicate creation
                if (uniquedbcon == null){
                    uniquedbcon = new DBConnector();
                }
            }
        }
        return uniquedbcon;
    }

    public void userConnect(){
        System.out.println("user is connected to db! : Object @ = " + uniquedbcon);
    }
}
```

```java
package com.java.course;

public class Main {
    public static void main(String[] args) {
        System.out.println("Creating a singleton connection to DB");
        DBConnector dbConnector = DBConnector.getInstance();
        dbConnector.userConnect();
    }
}
```

### How It Works — Step by Step
1. First call: Thread A checks `uniquedbcon == null` → true
2. Thread A enters the synchronized block, checks again → still null
3. Thread A creates the instance and assigns it to `uniquedbcon`
4. Meanwhile, Thread B also checks `uniquedbcon == null` → true (before A finishes)
5. Thread B tries to enter synchronized block — blocked until A exits
6. Thread B enters, checks again → NOT null (A already created it) → skips creation
7. All subsequent calls: first check returns false → no lock acquired → fast return

### Why `volatile` is Critical
Without `volatile`, the JVM can reorder instructions during `new DBConnector()`:
1. Allocate memory
2. Assign reference to `uniquedbcon` ← another thread sees non-null here
3. Call constructor ← but object isn't fully constructed yet!

`volatile` establishes a happens-before relationship that prevents this reordering.

### Pitfalls and Common Mistakes
- **Forgetting volatile:** The pattern is BROKEN without `volatile` on Java 5+. Threads can see a partially constructed object
- **Pre-Java 5:** This pattern doesn't work reliably before Java 5 due to the old memory model
- **Complexity:** For most cases, eager initialization or the enum singleton is simpler and sufficient

### Connection to Other Patterns
- This is the performance-optimized version of the **Lazy Singleton**
- Modern alternative: **Initialization-on-demand holder idiom** (static inner class) achieves the same with less complexity
- Joshua Bloch recommends **Enum Singleton** as the best approach in Effective Java

---

## Simple Factory — Hamburger

**GoF Category:** Creational

![Factory Diagram](06_HamburgerFactoryPattern/HamburgerFactoryPattern/Diagram.jpg)
![Factory Diagram 2](06_HamburgerFactoryPattern/HamburgerFactoryPattern/Diagram2.jpg)
![Factory Diagram 3](06_HamburgerFactoryPattern/HamburgerFactoryPattern/Diagram3.jpg)

### Intent
Encapsulates object creation logic in a separate factory class, decoupling the client from concrete product classes. The client asks the factory for an object by type without knowing which concrete class is instantiated.

### When to Use
- When you have multiple related classes and the client shouldn't know which one to instantiate
- When creation logic is complex or involves conditional decisions
- When you want to centralize creation to make it easy to add new types
- Restaurant ordering systems, document creators, UI widget factories

### Key Participants
| Class | Role |
|-------|------|
| `Hamburger` | Abstract product — defines the product interface |
| `CheeseBurger`, `GreekBurger`, `MeatLover`, `VeggieBurger`, `BunLessBurger` | Concrete products |
| `SimpleHamburgerFactory` | Factory — encapsulates creation logic |
| `JamaicanHambugerFactory` | Extended factory for regional variants |
| `HamburgerStore` | Client — uses the factory without knowing concrete classes |

### Complete Source Code

```java
package com.kejeiri.model;

// Abstract product — defines what all hamburgers can do
public abstract class Hamburger {
    public void prepare(){}  // Template method hook
    public void cook(){}     // Template method hook
    public void box(){}      // Template method hook
}
```

```java
package com.kejeiri.Core;
import com.kejeiri.model.*;

// The factory — centralizes creation logic using a type discriminator
public class SimpleHamburgerFactory {
    public static final String CHEESE="cheese";
    public static final String GREEK="greek";
    public static final String MEAT="meatlover";
    public static final String VEGGIE="veggie";
    public static final String BUNLESS="bunless";

    public Hamburger createHamburger(String type){
        Hamburger burger = null;
        switch (type) {
            case CHEESE: burger = new CheeseBurger(); break;
            case GREEK: burger = new GreekBurger(); break;
            case MEAT: burger = new MeatLover(); break;
            case VEGGIE: burger = new VeggieBurger(); break;
            case BUNLESS: burger = new BunLessBurger(); break;
            default: throw new NotImplementedException();
        }
        return burger;
    }
}
```

```java
package com.kejeiri.Core;
import com.kejeiri.model.Hamburger;

// Extended factory — subclasses can override to provide regional variants
public class JamaicanHambugerFactory extends SimpleHamburgerFactory {
    @Override
    public Hamburger createHamburger(String type) {
        // Could return JamaicanCheeseBurger, JamaicanGreekBurger, etc.
        return super.createHamburger(type);
    }
}
```

```java
package com.kejeiri.Core;
import com.kejeiri.model.Hamburger;

// Client — depends on the factory abstraction, not concrete products
public class HamburgerStore {
    private SimpleHamburgerFactory simpleHamburgerFactory;

    public HamburgerStore(SimpleHamburgerFactory simpleHamburgerFactory) {
        this.simpleHamburgerFactory = simpleHamburgerFactory;
    }

    public Hamburger orderHamburger(String type){
        System.out.println("Ordering "+ type + " burger");
        // Delegates creation to the factory
        Hamburger burger = simpleHamburgerFactory.createHamburger(type);
        // Uses the product through the abstract interface
        burger.prepare();
        burger.cook();
        burger.box();
        System.out.println("picking up order");
        return burger;
    }
}
```

```java
package com.kejeiri;
import com.kejeiri.Core.HamburgerStore;
import com.kejeiri.Core.JamaicanHambugerFactory;

public class Main {
    public static void main(String[] args) {
        // Inject a specific factory — the store doesn't know which burgers it creates
        JamaicanHambugerFactory jamaicanHambugerFactory = new JamaicanHambugerFactory();
        HamburgerStore hs = new HamburgerStore(jamaicanHambugerFactory);
        hs.orderHamburger("cheese");
    }
}
```

### How It Works — Step by Step
1. `Main` creates a `JamaicanHambugerFactory` and injects it into `HamburgerStore`
2. When `orderHamburger("cheese")` is called, the store delegates to `factory.createHamburger("cheese")`
3. The factory's switch statement maps the string type to a concrete class (`CheeseBurger`)
4. The store receives a `Hamburger` reference — it doesn't know or care it's a `CheeseBurger`
5. The store calls `prepare()`, `cook()`, `box()` through the abstract interface

### Pitfalls and Common Mistakes
- **Open/Closed violation:** Adding a new burger type requires modifying the factory's switch statement
- **String-based type discrimination:** Typos cause runtime errors. Use enums instead
- **Simple Factory vs Factory Method:** Simple Factory is NOT a GoF pattern — it's a programming idiom. The Factory Method pattern uses inheritance (subclass decides what to create)

### Connection to Other Patterns
- **Factory Method** (pattern 07) makes the factory method abstract, letting subclasses decide
- **Abstract Factory** creates families of related objects
- Often combined with **Template Method** — the product's lifecycle methods (prepare, cook, box) form a template

---

## Factory Method — Enhanced Hamburger

**GoF Category:** Creational

![Factory Method Diagram 1](07_HamburgerFactoryPattern_ENHANCED/HamburgerFactoryPattern/Diagram1.jpg)
![Factory Method Diagram 2](07_HamburgerFactoryPattern_ENHANCED/HamburgerFactoryPattern/Diagram2.jpg)
![Factory Method Figure](07_HamburgerFactoryPattern_ENHANCED/HamburgerFactoryPattern/figure.jpg)

### Intent
Defines an interface for creating objects but lets subclasses decide which class to instantiate. Unlike Simple Factory, the creation method is meant to be overridden by subclasses, each providing their own product variants.

### When to Use
- When a class can't anticipate which objects it needs to create
- When you want subclasses to specify the objects they create
- When you need regional/contextual variants of products (e.g., Jamaican-style vs American-style burgers)
- Framework code that defines the workflow but lets plugins define the objects

### Key Participants
| Class | Role |
|-------|------|
| `SimpleHamburgerFactory` | Creator — declares the factory method |
| `JamaicanHambugerFactory` | Concrete Creator — overrides factory method for regional variants |
| `Hamburger` | Product interface |
| Concrete burgers | Concrete Products |

### Complete Source Code
*(Same structure as pattern 06 — the key difference is that `JamaicanHambugerFactory` is designed to override `createHamburger()` to return Jamaican-specific burger subclasses)*

```java
package com.kejeiri.Core;
import com.kejeiri.model.Hamburger;

// Factory Method pattern: subclass overrides creation to provide variants
public class JamaicanHambugerFactory extends SimpleHamburgerFactory {
    @Override
    public Hamburger createHamburger(String type) {
        // In a full implementation, this would return:
        // case CHEESE: return new JamaicanCheeseBurger(); // jerk seasoning
        // case VEGGIE: return new JamaicanVeggieBurger(); // ackee & callaloo
        return super.createHamburger(type);
    }
}
```

### How It Works — Step by Step
1. `SimpleHamburgerFactory` defines `createHamburger()` as a virtual method (non-final)
2. `JamaicanHambugerFactory` extends it and overrides `createHamburger()`
3. The `HamburgerStore` holds a reference typed as `SimpleHamburgerFactory`
4. At runtime, polymorphism ensures the correct factory's `createHamburger()` is called
5. Each regional factory returns its own product variants without changing the store

### Pitfalls and Common Mistakes
- **Parallel class hierarchies:** Each new product requires a new factory subclass — can lead to class explosion
- **Confusion with Simple Factory:** Simple Factory uses a concrete class with conditional logic; Factory Method uses inheritance and polymorphism

### Connection to Other Patterns
- **Abstract Factory** is often implemented with Factory Methods
- **Template Method** — the `orderHamburger()` method is a template that calls the factory method as a hook
- **Prototype** can be an alternative when subclassing for each variant is too heavy

---

## Builder — User

**GoF Category:** Creational

### Intent
Separates the construction of a complex object from its representation, allowing the same construction process to create different representations. Particularly useful when an object has many optional parameters — avoids telescoping constructors.

### When to Use
- Objects with many optional parameters (the "telescoping constructor" problem)
- When object construction requires multiple steps
- When you want immutable objects that are complex to construct
- Building SQL queries, HTTP requests, UI layouts, configuration objects

### Key Participants
| Class | Role |
|-------|------|
| `User` | Product — the complex object being built (immutable) |
| `User.UserBuilder` | Builder — static inner class with fluent API |

### Complete Source Code

```java
package com.kejeiri.java.course;

public class User {
    // All fields are final — the built object is immutable
    private final String firstName;
    private final String lastName;
    private final int age;
    private final String address;
    private final String phone;

    // Private constructor — only the builder can create User instances
    public User(UserBuilder builder) {
        this.firstName = builder.firstName;
        this.lastName = builder.lastName;
        this.age = builder.age;
        this.address = builder.address;
        this.phone = builder.phone;
    }

    @Override
    public String toString() {
        return "Name: " + firstName +" "+lastName + "\nage:" + age
            + ", address: " +address + ", phone: "+phone ;
    }

    // Static inner Builder class
    public static class UserBuilder{
        // Required parameters — set in constructor
        private final String firstName;
        private final String lastName;

        // Optional parameters — set via fluent methods
        private int age;
        private String address;
        private String phone;

        // Builder constructor takes only required params
        public UserBuilder(String firstName, String lastName) {
            this.firstName = firstName;
            this.lastName = lastName;
        }

        // Each setter returns 'this' for method chaining
        public UserBuilder age (int age) { this.age = age; return this; }
        public UserBuilder address(String address) { this.address = address; return this; }
        public UserBuilder phone (String phone) { this.phone = phone; return this; }

        // Terminal operation — constructs the immutable User
        public User build() { return new User(this); }
    }
}
```

```java
package com.kejeiri.java.course;

public class Main {
    public static void main(String[] args) {
        // Fluent API — reads like a sentence, optional params are clear
        User user = new User.UserBuilder("Mohamed","kejeiri")
                .age(40)
                .address("Brussels")
                .phone("+34545477888")
                .build();
        System.out.println(user);
    }
}
```

### How It Works — Step by Step
1. Client creates a `UserBuilder` with required parameters (firstName, lastName)
2. Client chains optional parameter methods: `.age(40).address("Brussels")`
3. Each method sets the field and returns `this` (the builder itself)
4. Client calls `.build()` which creates a new `User`, passing the builder to User's constructor
5. `User`'s constructor copies all values from the builder into final fields
6. The resulting `User` object is immutable — no setters exist

### Pitfalls and Common Mistakes
- **Forgetting to call build():** The builder is not the product — you must call `build()` to get the actual object
- **Mutable builder reuse:** If you reuse a builder and change values between builds, you get different objects (which may be intentional or a bug)
- **Validation:** Add validation in `build()` before constructing the object — throw `IllegalStateException` for invalid combinations
- **Boilerplate:** Lots of code for simple objects. Use Lombok's `@Builder` in production

### Connection to Other Patterns
- **Telescoping Constructor anti-pattern** is what Builder solves
- **Abstract Factory** can use Builder to construct complex products
- **Prototype** is an alternative when you want to copy an existing object rather than build from scratch
- In practice, Lombok's `@Builder` or records (Java 16+) reduce the boilerplate

---

## Builder — (Variant 21)

**GoF Category:** Creational

### Intent
Same as pattern 20. This variant demonstrates the Builder pattern in a different domain context, reinforcing the same principles: fluent API, separation of construction from representation, and handling of optional parameters.

*(The repo's pattern 21 follows the identical Builder structure as pattern 20 applied to a different domain object)*

---

## Prototype

**GoF Category:** Creational

![Prototype Figure 1](22_PrototypeDesignPattern/PrototypeDesignPattern/figure1.jpg)
![Prototype Figure 2](22_PrototypeDesignPattern/PrototypeDesignPattern/figure2.jpg)

### Intent
Creates new objects by copying an existing object (the prototype) rather than instantiating from scratch. Useful when object creation is expensive or when you need copies with slight variations.

### When to Use
- When object creation is costly (database calls, network requests, complex computation)
- When you need many similar objects with minor differences
- When classes to instantiate are specified at runtime
- Game development (cloning enemy templates), document templates, cell biology simulations

### Key Participants
| Class | Role |
|-------|------|
| `Prototype` | Interface/abstract class declaring `clone()` |
| Concrete prototypes | Classes implementing the clone operation |
| Client | Creates new objects by asking prototypes to clone themselves |

### Complete Source Code
*(Pattern 22 in the repo implements Java's `Cloneable` interface)*

```java
// Prototype pattern uses Java's built-in clone mechanism
// or a custom copy constructor / copy method

public abstract class Shape implements Cloneable {
    private String id;
    protected String type;

    abstract void draw();

    public String getType() { return type; }
    public String getId() { return id; }
    public void setId(String id) { this.id = id; }

    // The key method — creates a copy of this object
    @Override
    public Object clone() {
        Object clone = null;
        try {
            clone = super.clone(); // Shallow copy
        } catch (CloneNotSupportedException e) {
            e.printStackTrace();
        }
        return clone;
    }
}
```

### How It Works — Step by Step
1. A prototype registry stores pre-built objects keyed by type
2. When a client needs a new object, it requests a clone from the registry
3. The prototype's `clone()` method creates a copy (shallow by default)
4. The client customizes the clone as needed
5. No `new` keyword or constructor knowledge required by the client

### Pitfalls and Common Mistakes
- **Shallow vs Deep copy:** `Object.clone()` performs shallow copy — reference fields still point to the same objects. For deep copy, manually clone nested objects
- **Cloneable is broken:** Joshua Bloch (Effective Java) considers `Cloneable` a broken interface. Prefer copy constructors or copy factory methods
- **Mutable shared state:** After shallow clone, mutating a nested object affects both original and clone

### Connection to Other Patterns
- Alternative to **Factory Method** when subclassing for each variant is too heavy
- Can be combined with **Registry/Cache** patterns to store prototypes
- **Builder** constructs step-by-step; **Prototype** copies an existing whole object


---

# Structural Patterns

Structural patterns deal with object composition — how classes and objects are composed to form larger structures while keeping them flexible and efficient.

---

## Adapter

**GoF Category:** Structural

![Adapter Diagram](12_AdapterPattern/AdapterPattern/diagram.jpg)
![Adapter Figure](12_AdapterPattern/AdapterPattern/figure.jpg)

### Intent
Converts the interface of a class into another interface that clients expect. Allows classes with incompatible interfaces to work together by wrapping one interface to look like another.

### When to Use
- Integrating legacy code with new systems
- Using third-party libraries whose interfaces don't match yours
- Wrapping vendor APIs behind your own interface for portability
- Converting XML to JSON, adapting database drivers, wrapping REST clients

### Key Participants
| Class | Role |
|-------|------|
| Target | The interface the client expects |
| Adaptee | The existing class with an incompatible interface |
| Adapter | Wraps the Adaptee and implements the Target interface |
| Client | Works with the Target interface |

### Complete Source Code
*(Pattern 12 in the repo)*

```java
// Target interface — what the client expects
public interface MediaPlayer {
    void play(String audioType, String fileName);
}

// Adaptee — has useful functionality but incompatible interface
public interface AdvancedMediaPlayer {
    void playVlc(String fileName);
    void playMp4(String fileName);
}

public class VlcPlayer implements AdvancedMediaPlayer {
    @Override
    public void playVlc(String fileName) {
        System.out.println("Playing vlc file: " + fileName);
    }
    @Override
    public void playMp4(String fileName) { /* do nothing */ }
}

public class Mp4Player implements AdvancedMediaPlayer {
    @Override
    public void playVlc(String fileName) { /* do nothing */ }
    @Override
    public void playMp4(String fileName) {
        System.out.println("Playing mp4 file: " + fileName);
    }
}

// Adapter — bridges the gap between MediaPlayer and AdvancedMediaPlayer
public class MediaAdapter implements MediaPlayer {
    AdvancedMediaPlayer advancedMediaPlayer;

    public MediaAdapter(String audioType) {
        if (audioType.equalsIgnoreCase("vlc")) {
            advancedMediaPlayer = new VlcPlayer();
        } else if (audioType.equalsIgnoreCase("mp4")) {
            advancedMediaPlayer = new Mp4Player();
        }
    }

    @Override
    public void play(String audioType, String fileName) {
        if (audioType.equalsIgnoreCase("vlc")) {
            advancedMediaPlayer.playVlc(fileName);
        } else if (audioType.equalsIgnoreCase("mp4")) {
            advancedMediaPlayer.playMp4(fileName);
        }
    }
}

// Client — uses MediaPlayer interface, unaware of AdvancedMediaPlayer
public class AudioPlayer implements MediaPlayer {
    MediaAdapter mediaAdapter;

    @Override
    public void play(String audioType, String fileName) {
        if (audioType.equalsIgnoreCase("mp3")) {
            System.out.println("Playing mp3 file: " + fileName);
        } else if (audioType.equalsIgnoreCase("vlc") || audioType.equalsIgnoreCase("mp4")) {
            mediaAdapter = new MediaAdapter(audioType);
            mediaAdapter.play(audioType, fileName);
        } else {
            System.out.println("Invalid media type: " + audioType);
        }
    }
}
```

### How It Works — Step by Step
1. `AudioPlayer` implements `MediaPlayer` and handles mp3 natively
2. For vlc/mp4 formats, it creates a `MediaAdapter`
3. `MediaAdapter` implements `MediaPlayer` but internally delegates to `AdvancedMediaPlayer`
4. The adapter translates `play(type, file)` calls into `playVlc(file)` or `playMp4(file)`
5. The client (`AudioPlayer`) never directly touches `AdvancedMediaPlayer`

### Pitfalls and Common Mistakes
- **Too many adapters:** If you're writing adapters everywhere, your interfaces may need redesigning
- **Object vs Class adapter:** Object adapter uses composition (preferred); Class adapter uses multiple inheritance (not possible in Java without interfaces)
- **Leaky abstractions:** The adapter should fully hide the adaptee's interface — don't expose adaptee-specific exceptions

### Connection to Other Patterns
- **Facade** simplifies a complex subsystem; **Adapter** makes one interface match another
- **Decorator** adds behavior; **Adapter** changes the interface
- **Bridge** is designed up-front to separate abstraction from implementation; **Adapter** is retrofitted

---

## Bridge

**GoF Category:** Structural

![Bridge Figure 1](28_BridgeDesignPattern/BridgeDesignPattern/figure1.jpg)
![Bridge Figure 2](28_BridgeDesignPattern/BridgeDesignPattern/figure2.jpg)

### Intent
Decouples an abstraction from its implementation so that the two can vary independently. Instead of a monolithic inheritance hierarchy, you split it into two separate hierarchies connected by composition.

### When to Use
- When you want to avoid a permanent binding between abstraction and implementation
- When both the abstraction and implementation should be extensible via subclassing
- When changes in implementation shouldn't affect client code
- Cross-platform UI toolkits, device drivers, rendering engines with multiple backends

### Key Participants
| Class | Role |
|-------|------|
| `Vehicle` | Abstraction — defines the high-level interface |
| `Car`, `Bike` | Refined Abstractions — extend Vehicle |
| `Workshop` | Implementor — defines the implementation interface |
| `Make`, `Assemble` | Concrete Implementors — provide specific implementations |

### Complete Source Code

```java
package com.java.course;

// Implementor interface — defines what implementations must provide
interface Workshop {
    void make();
}
```

```java
package com.java.course;

// Concrete Implementor A — manufacturing step
public class Make implements Workshop{
    @Override
    public void make() { System.out.println("Making..."); }
}
```

```java
package com.java.course;

// Concrete Implementor B — assembly step
public class Assemble implements Workshop {
    @Override
    public void make() {
        System.out.print("...also");
        System.out.println("...Assembled");
    }
}
```

```java
package com.java.course;

// Abstraction — holds references to implementors (the "bridge")
abstract class Vehicle {
    Workshop manufactureLine;  // Bridge to implementation
    Workshop assemblyLine;     // Bridge to implementation

    public Vehicle(Workshop manufactureLine, Workshop assemblyLine) {
        this.manufactureLine = manufactureLine;
        this.assemblyLine = assemblyLine;
    }

    public abstract void manufucture();
}
```

```java
package com.java.course;

// Refined Abstraction — Car
public class Car extends Vehicle{
    public Car(Workshop manufactureLine, Workshop assemblyLine) {
        super(manufactureLine, assemblyLine);
    }

    @Override
    public void manufucture() {
        System.out.println("Car...");
        manufactureLine.make();  // Delegates to implementor
        assemblyLine.make();     // Delegates to implementor
    }
}
```

```java
package com.java.course;

// Refined Abstraction — Bike
public class Bike extends Vehicle{
    public Bike(Workshop manufactureLine, Workshop assemblyLine) {
        super(manufactureLine, assemblyLine);
    }

    @Override
    public void manufucture() {
        System.out.println("Bike...");
        manufactureLine.make();
        assemblyLine.make();
    }
}
```

```java
package com.java.course;

public class Main {
    public static void main(String[] args) {
        // Compose abstraction with implementations at runtime
        Vehicle audi = new Car(new Make(), new Assemble());
        audi.manufucture();

        Vehicle vtt = new Bike(new Make(), new Assemble());
        vtt.manufucture();
    }
}
```

### How It Works — Step by Step
1. `Workshop` defines the implementor interface with a single `make()` method
2. `Make` and `Assemble` are concrete implementors providing specific behavior
3. `Vehicle` (abstraction) holds references to `Workshop` objects — this is the "bridge"
4. `Car` and `Bike` extend `Vehicle` and implement `manufucture()` by delegating to the workshop references
5. In `Main`, vehicles are composed with specific workshops at runtime
6. You can add new vehicles (Truck) OR new workshops (Paint) without modifying existing code

### Pitfalls and Common Mistakes
- **Over-engineering:** Don't use Bridge when you only have one implementation — it adds unnecessary indirection
- **Confusion with Strategy:** Bridge separates abstraction from implementation at the architectural level; Strategy swaps algorithms at the behavioral level
- **Identifying the split:** The hardest part is recognizing which dimension to split into abstraction vs implementation

### Connection to Other Patterns
- **Adapter** makes unrelated classes work together; **Bridge** is designed up-front to let abstraction and implementation vary
- **Strategy** is similar in structure but different in intent — Strategy is about interchangeable algorithms; Bridge is about separating concerns
- **Abstract Factory** can create the implementor objects that the Bridge uses

---

## Decorator

**GoF Category:** Structural

![Decorator Diagram 1](05_icecreamdecoratorpattern/decoratorpattern/Diagram1.jpg)
![Decorator Diagram 2](05_icecreamdecoratorpattern/decoratorpattern/Diagram2.jpg)
![Decorator Diagram 3](05_icecreamdecoratorpattern/decoratorpattern/Diagram3.jpg)

### Intent
Attaches additional responsibilities to an object dynamically. Provides a flexible alternative to subclassing for extending functionality. Decorators wrap the original object and add behavior before/after delegating to it.

### When to Use
- When you need to add responsibilities to objects dynamically without affecting other objects
- When extension by subclassing is impractical (too many combinations)
- Java I/O streams (`BufferedInputStream` wrapping `FileInputStream`)
- Adding logging, caching, encryption, compression to existing services

### Key Participants
| Class | Role |
|-------|------|
| `IceCream` | Component interface — defines the contract |
| `BasicIceCream` | Concrete Component — the base object being decorated |
| `IceCreamDecorator` | Abstract Decorator — wraps a Component and delegates |
| `MintIceCream`, `VanillaIceCream`, `PeanutIceCream` | Concrete Decorators — add specific behavior |

### Complete Source Code

```java
package com.kejeiri.java.course.imodel;

// Component interface — both the base object and decorators implement this
public interface IceCream {
    double cost();
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.imodel.IceCream;

// Concrete Component — the base object that gets decorated
public class BasicIceCream implements IceCream {
    public BasicIceCream() { System.out.println("basic Icecream is created"); }
    @Override
    public double cost() { return 0.5; }
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.imodel.IceCream;

// Abstract Decorator — implements the same interface and wraps a component
public abstract class IceCreamDecorator implements IceCream {
    private IceCream iceCream;  // The wrapped component (could be base or another decorator)

    public IceCreamDecorator(IceCream iceCream) { this.iceCream = iceCream; }

    @Override
    public double cost() { return this.iceCream.cost(); }  // Delegates to wrapped object
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.imodel.IceCream;

// Concrete Decorator — adds mint flavor cost
public class MintIceCream extends IceCreamDecorator{
    public MintIceCream(IceCream iceCream) { super(iceCream); }
    @Override
    public double cost() {
        System.out.println("Adding mint Ice-cream!");
        return 1.50 + super.cost();  // Adds own cost + delegates to wrapped
    }
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.imodel.IceCream;

// Concrete Decorator — adds vanilla flavor cost
public class VanillaIceCream extends IceCreamDecorator{
    public VanillaIceCream(IceCream iceCream) { super(iceCream); }
    @Override
    public double cost() {
        System.out.println("Adding vanilla Ice-cream!");
        return 1.00 + super.cost();
    }
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.imodel.IceCream;

// Concrete Decorator — adds peanut topping cost
public class PeanutIceCream extends IceCreamDecorator{
    public PeanutIceCream(IceCream iceCream) { super(iceCream); }
    @Override
    public double cost() {
        System.out.println("Adding peanut Ice-cream!");
        return 2.00 + super.cost();
    }
}
```

```java
package com.kejeiri.java.course;
import com.kejeiri.java.course.imodel.IceCream;
import com.kejeiri.java.course.model.*;

public class Main {
    public static void main(String[] args) {
        // Start with base component
        IceCream basicIceCream = new BasicIceCream();
        System.out.println("Basic icecream cost: $"+basicIceCream.cost());

        // Wrap with vanilla decorator
        IceCream vanilla = new VanillaIceCream(basicIceCream);
        System.out.println("vanilla icecream cost: $"+vanilla.cost());

        // Wrap vanilla with mint decorator (stacking!)
        IceCream mint = new MintIceCream(vanilla);
        System.out.println("adding mint icecream cost: $"+mint.cost());

        // Wrap mint+vanilla with peanut decorator (triple stack!)
        IceCream peanut = new PeanutIceCream(mint);
        System.out.println("adding peanut icecream cost: $"+peanut.cost());
        // Final cost: 0.5 (basic) + 1.0 (vanilla) + 1.5 (mint) + 2.0 (peanut) = $5.0
    }
}
```

### How It Works — Step by Step
1. `BasicIceCream` costs $0.50 — this is the core component
2. `VanillaIceCream` wraps `BasicIceCream` — its `cost()` returns `1.00 + wrapped.cost()` = $1.50
3. `MintIceCream` wraps the vanilla-wrapped-basic — returns `1.50 + wrapped.cost()` = $3.00
4. `PeanutIceCream` wraps the whole chain — returns `2.00 + wrapped.cost()` = $5.00
5. Each decorator is transparent — the client always works with the `IceCream` interface
6. Decorators can be stacked in any order and any combination

### Pitfalls and Common Mistakes
- **Identity checks fail:** `decoratedObj == originalObj` is false. Don't use `==` or rely on object identity
- **Order matters:** Decorators are applied in order. Encryption-then-compression ≠ compression-then-encryption
- **Too many small classes:** Each decorator is a class. For simple cases, consider lambdas or functional composition
- **Debugging difficulty:** Deep decorator chains make stack traces hard to read

### Connection to Other Patterns
- **Adapter** changes interface; **Decorator** adds behavior while keeping the same interface
- **Composite** has similar recursive structure but for tree hierarchies
- **Strategy** changes the guts of an object; **Decorator** changes the skin
- Java I/O is the canonical real-world example: `new BufferedReader(new InputStreamReader(new FileInputStream(f)))`

---

## Facade

**GoF Category:** Structural

![Facade Diagram](13_FacadePattern/FacadePattern/Diagram.jpg)
![Facade Figure](13_FacadePattern/FacadePattern/figure.jpg)

### Intent
Provides a unified, simplified interface to a complex subsystem. Reduces coupling between clients and the subsystem by hiding its complexity behind a single entry point.

### When to Use
- When a subsystem has many interdependent classes and the client only needs a simple interface
- When you want to layer your system (each layer has a facade)
- Wrapping complex library APIs (e.g., a `VideoConverter` facade over codec, bitrate, format classes)
- Service layers in enterprise applications that hide repository/entity complexity

### Key Participants
| Class | Role |
|-------|------|
| Facade | Provides simplified methods that delegate to subsystem classes |
| Subsystem classes | The complex internal classes that do the real work |
| Client | Uses only the Facade, unaware of subsystem complexity |

### Complete Source Code
*(Pattern 13 in the repo)*

```java
// Subsystem class 1
public class CPU {
    public void freeze() { System.out.println("CPU frozen"); }
    public void jump(long position) { System.out.println("CPU jumping to " + position); }
    public void execute() { System.out.println("CPU executing"); }
}

// Subsystem class 2
public class Memory {
    public void load(long position, byte[] data) {
        System.out.println("Memory loading data at " + position);
    }
}

// Subsystem class 3
public class HardDrive {
    public byte[] read(long lba, int size) {
        System.out.println("HardDrive reading sector " + lba);
        return new byte[size];
    }
}

// Facade — hides the complexity of booting a computer
public class ComputerFacade {
    private CPU cpu;
    private Memory memory;
    private HardDrive hardDrive;

    public ComputerFacade() {
        this.cpu = new CPU();
        this.memory = new Memory();
        this.hardDrive = new HardDrive();
    }

    // Simple method that orchestrates complex subsystem interactions
    public void start() {
        cpu.freeze();
        memory.load(0, hardDrive.read(0, 1024));
        cpu.jump(0);
        cpu.execute();
    }
}

// Client — only knows about the Facade
public class Main {
    public static void main(String[] args) {
        ComputerFacade computer = new ComputerFacade();
        computer.start();  // One simple call instead of 4 complex ones
    }
}
```

### How It Works — Step by Step
1. The subsystem has multiple classes (CPU, Memory, HardDrive) with complex interactions
2. `ComputerFacade` creates and holds references to all subsystem objects
3. `start()` orchestrates the correct sequence of subsystem calls
4. The client calls one method (`start()`) instead of managing the boot sequence manually
5. The subsystem classes are still accessible directly if advanced clients need them

### Pitfalls and Common Mistakes
- **God object:** Don't let the facade grow into a massive class that does everything — split into multiple facades
- **Hiding too much:** The facade should simplify, not prevent access. Advanced clients should still be able to use subsystem classes directly
- **Tight coupling inside facade:** The facade itself becomes coupled to the subsystem — if the subsystem changes, only the facade needs updating (which is the point)

### Connection to Other Patterns
- **Adapter** changes an interface; **Facade** simplifies an interface
- **Mediator** coordinates between colleagues; **Facade** provides a one-way simplified interface
- Often implemented as a **Singleton** since usually only one facade is needed
- **Abstract Factory** can be used as an alternative to Facade for hiding platform-specific classes

---

## Flyweight

**GoF Category:** Structural

![Flyweight Figure](29_FlyWeightDesignPattern/FlyWeightDesignPattern/figure1.jpg)

### Intent
Minimizes memory usage by sharing as much data as possible between similar objects. Separates intrinsic state (shared, immutable) from extrinsic state (unique, context-dependent) to enable massive object reuse.

### When to Use
- When an application uses a large number of similar objects
- When storage costs are high due to the sheer quantity of objects
- When most object state can be made extrinsic (passed in from outside)
- Text editors (character objects), game engines (tree/particle objects), GIS systems (map tiles)

### Key Participants
| Class | Role |
|-------|------|
| `Shape` | Flyweight interface |
| `Circle` | Concrete Flyweight — stores intrinsic state (color), accepts extrinsic state (x, y, radius) |
| `ShapeFactory` | Flyweight Factory — creates and caches flyweight objects |

### Complete Source Code

```java
package com.java.course;

// Flyweight interface
public interface Shape {
    void draw();
}
```

```java
package com.java.course;

// Concrete Flyweight
public class Circle implements Shape {
    private String color;   // INTRINSIC state — shared, set at creation, never changes
    private int x;          // EXTRINSIC state — varies per use, set externally
    private int y;          // EXTRINSIC state
    private int radius;     // EXTRINSIC state

    // Only intrinsic state is set in constructor
    public Circle(String color) { this.color = color; }

    public String getColor() { return color; }
    public void setColor(String color) { this.color = color; }
    public int getX() { return x; }
    public void setX(int x) { this.x = x; }
    public int getY() { return y; }
    public void setY(int y) { this.y = y; }
    public int getRadius() { return radius; }
    public void setRadius(int radius) { this.radius = radius; }

    @Override
    public void draw() {
        System.out.print("Drawing circle... ");
        System.out.print(", Color: = " + color);
        System.out.print(", X: = " + x);
        System.out.print(", Y: = " + y);
        System.out.println(", Radius: = " + radius);
    }
}
```

```java
package com.java.course;

import java.util.HashMap;

// Flyweight Factory — manages the pool of shared objects
public class ShapeFactory {
    // Cache: key = intrinsic state (color), value = shared Circle instance
    private static final HashMap<String, Circle> circleMap = new HashMap<>();

    public static Shape getCircle(String color){
        Circle circle = circleMap.get(color);
        if (circle == null){
            // Only create a new object if one doesn't exist for this color
            circle = new Circle(color);
            circleMap.put(color, circle);
            System.out.println("Making circle of color: " + color);
        }
        return circle;  // Return shared instance
    }
}
```

```java
package com.java.course;

public class Main {
    private static final String colors[] = {"red","blue","green","pink","brown"};

    public static void main(String[] args) {
        ShapeFactory shapeFactory = new ShapeFactory();
        Circle circle;
        // 20 iterations but only up to 5 Circle objects created (one per color)
        for (int i = 1; i < 21; i++) {
            circle = (Circle) shapeFactory.getCircle(getRandomColor());
            // Extrinsic state set externally on each use
            circle.setX(getRandomX());
            circle.setY(getRandomY());
            circle.setRadius(400);
            circle.draw();
        }
    }

    public static String getRandomColor(){
        double d = Math.random() * colors.length;
        return colors[(int)d];
    }

    private static int getRandomX(){
        double d = Math.random() * 100;
        return (int) d;
    }

    private static int getRandomY(){
        double d = Math.random() * 100;
        return (int) d;
    }
}
```

### How It Works — Step by Step
1. `ShapeFactory` maintains a `HashMap` of Circle objects keyed by color (intrinsic state)
2. When `getCircle("red")` is called the first time, a new Circle is created and cached
3. Subsequent calls for "red" return the SAME Circle instance from the cache
4. The client sets extrinsic state (x, y, radius) on the shared instance before each use
5. Result: 20 draw operations use only 5 Circle objects (one per color)
6. Memory savings: instead of 20 objects, only 5 exist

### Pitfalls and Common Mistakes
- **Thread safety:** If extrinsic state is set on the shared object (as in this example), concurrent access is UNSAFE. In production, pass extrinsic state as method parameters instead of setters
- **Mutating intrinsic state:** Never change the shared state after creation — it affects all users
- **Premature optimization:** Only use Flyweight when you actually have memory pressure from many similar objects
- **Identity confusion:** `==` comparisons will be true for same-color circles, which may surprise code that expects distinct objects

### Connection to Other Patterns
- **Factory** is used to manage the flyweight pool
- **Composite** often uses Flyweight for leaf nodes (e.g., characters in a document)
- **State** and **Strategy** objects are often flyweights (shared, stateless)
- `String.intern()` in Java is a built-in flyweight implementation

---

## Proxy

**GoF Category:** Structural

![Proxy Diagram 1](18_ProxyPattern/ProxyPattern/Diagram1.jpg)
![Proxy Diagram 2](18_ProxyPattern/ProxyPattern/Diagram2.jpg)
![Proxy Figure 1](18_ProxyPattern/ProxyPattern/figure1.jpg)

### Intent
Provides a surrogate or placeholder for another object to control access to it. The proxy has the same interface as the real object, so the client doesn't know it's talking to a proxy.

### When to Use
- **Protection proxy:** Control access based on permissions (this example)
- **Virtual proxy:** Delay expensive object creation until actually needed
- **Remote proxy:** Represent an object in a different address space (RMI)
- **Caching proxy:** Cache results of expensive operations
- Security checks, lazy loading, logging, transaction management

### Key Participants
| Class | Role |
|-------|------|
| `IBank` | Subject interface — defines the contract |
| `RealBank` | Real Subject — the actual service |
| `ProxyBank` | Proxy — controls access to RealBank |

### Complete Source Code

```java
package com.java.course;

// Subject interface — both real and proxy implement this
public interface IBank {
    void withdrawMoney(String clientName) throws Exception;
}
```

```java
package com.java.course;
import java.util.ArrayList;

// Real Subject — performs the actual withdrawal
public class RealBank implements IBank{
    @Override
    public void withdrawMoney(String clientName) throws Exception {
        System.out.println(clientName + " is withdrawing from ATM...");
    }
}
```

```java
package com.java.course;
import java.util.ArrayList;

// Protection Proxy — checks access before delegating to RealBank
public class ProxyBank implements IBank{
    private RealBank bank = new RealBank();  // Holds reference to real subject

    // Access control list
    private static ArrayList bannedClient = new ArrayList<>();
    static{
        bannedClient.add("xxcs");
        bannedClient.add("me@me");
        bannedClient.add("@xmil.com");
    }

    @Override
    public void withdrawMoney(String clientName) throws Exception {
        // Access check — the proxy's added responsibility
        if (bannedClient.contains(clientName.toLowerCase())) {
            throw new Exception("Access denied for " + clientName);
        }
        // If allowed, delegate to the real subject
        bank.withdrawMoney(clientName);
    }
}
```

```java
package com.java.course;

public class Main {
    public static void main(String[] args) {
        // Client uses IBank interface — doesn't know it's a proxy
        IBank bank = new ProxyBank();
        try {
            bank.withdrawMoney("kejeiri");  // Allowed — delegates to RealBank
            bank.withdrawMoney("me@me");    // Banned — throws exception
        } catch (Exception e) {
            System.out.println(e.getMessage());
        }
    }
}
```

### How It Works — Step by Step
1. `IBank` defines the interface that both `RealBank` and `ProxyBank` implement
2. `ProxyBank` holds a reference to `RealBank` (composition)
3. When `withdrawMoney()` is called on the proxy, it first checks the banned list
4. If the client is banned, the proxy throws an exception — never reaching `RealBank`
5. If allowed, the proxy delegates to `RealBank.withdrawMoney()`
6. The client (`Main`) only knows about `IBank` — it's unaware of the proxy layer

### Pitfalls and Common Mistakes
- **Performance overhead:** Every call goes through the proxy. For high-frequency calls, this adds latency
- **Complexity:** Adding proxies for every service can make the codebase harder to navigate
- **Proxy vs Decorator confusion:** Both wrap objects, but Proxy controls access while Decorator adds behavior
- **Stale state in caching proxy:** Cached data can become outdated — implement invalidation

### Connection to Other Patterns
- **Decorator** has the same structure but different intent — Decorator adds responsibilities; Proxy controls access
- **Adapter** changes the interface; **Proxy** keeps the same interface
- **Facade** simplifies a subsystem; **Proxy** controls access to a single object
- Spring AOP uses dynamic proxies extensively for `@Transactional`, `@Cacheable`, etc.


---

# Behavioral Patterns

Behavioral patterns are concerned with algorithms and the assignment of responsibilities between objects. They describe patterns of communication between objects.

---

## Strategy — ScoreBoard

**GoF Category:** Behavioral

![Strategy Diagram](01_scoreBoard_strategy/Diagram.jpg)
![Strategy Figure](01_scoreBoard_strategy/figure.jpg)

### Intent
Defines a family of algorithms, encapsulates each one, and makes them interchangeable. Strategy lets the algorithm vary independently from the clients that use it. The context delegates work to a strategy object instead of implementing the algorithm directly.

### When to Use
- When you have multiple algorithms for a specific task and want to switch between them at runtime
- When you want to avoid conditional statements (if/else, switch) for selecting behavior
- Sorting algorithms, compression algorithms, route calculation, tax calculation, validation rules

### Key Participants
| Class | Role |
|-------|------|
| `ScoreBoardBase` | Abstract Strategy — declares the algorithm interface |
| `Balloon`, `Clown`, `SquareBalloon` | Concrete Strategies — implement specific algorithms |
| `ScoreBoard` | Context — maintains a reference to a strategy and delegates |

### Complete Source Code

```java
package com.kejeiri.controller;

// Abstract Strategy — defines the contract for all scoring algorithms
public abstract class ScoreBoardBase {
    public abstract int calculateScore(int taps, int multiplier);
}
```

```java
package com.kejeiri.controller;

// Context — holds a strategy reference and delegates calculation
public class ScoreBoard {
    public ScoreBoardBase scoreBoardBase;  // The current strategy

    public void show(int taps, int mulitplier){
        // Delegates to whatever strategy is currently set
        System.out.println(scoreBoardBase.calculateScore(taps, mulitplier));
    }
}
```

```java
package com.kejeiri.Model;
import com.kejeiri.controller.ScoreBoardBase;

// Concrete Strategy A — balloon scoring: penalizes by 20
public class Balloon extends ScoreBoardBase {
    @Override
    public int calculateScore(int taps, int multiplier) {
        return (taps * multiplier) - 20;
    }
}
```

```java
package com.kejeiri.Model;
import com.kejeiri.controller.ScoreBoardBase;

// Concrete Strategy B — clown scoring: penalizes by 10
public class Clown extends ScoreBoardBase {
    @Override
    public int calculateScore(int taps, int multiplier) {
        return (taps * multiplier) - 10;
    }
}
```

```java
package com.kejeiri.Model;
import com.kejeiri.controller.ScoreBoardBase;

// Concrete Strategy C — square balloon scoring: bonus of 40
public class SquareBalloon extends ScoreBoardBase {
    @Override
    public int calculateScore(int taps, int multiplier) {
        return (taps * multiplier) + 40;
    }
}
```

```java
package com.kejeiri;
import com.kejeiri.Model.Balloon;
import com.kejeiri.Model.Clown;
import com.kejeiri.Model.SquareBalloon;
import com.kejeiri.controller.ScoreBoard;

public class Main {
    public static void main(String[] args) {
        ScoreBoard scoreBoard = new ScoreBoard();

        // Swap strategy at runtime — same context, different algorithm
        System.out.print("Balloon taps score: ");
        scoreBoard.scoreBoardBase = new Balloon();
        scoreBoard.show(10, 78);  // (10*78)-20 = 760

        System.out.print("Clown taps score: ");
        scoreBoard.scoreBoardBase = new Clown();
        scoreBoard.show(10, 78);  // (10*78)-10 = 770

        System.out.print("SquareBalloon taps score: ");
        scoreBoard.scoreBoardBase = new SquareBalloon();
        scoreBoard.show(10, 78);  // (10*78)+40 = 820
    }
}
```

### How It Works — Step by Step
1. `ScoreBoardBase` declares `calculateScore()` — the algorithm contract
2. Three concrete strategies implement different scoring formulas
3. `ScoreBoard` (context) holds a `ScoreBoardBase` reference
4. The client assigns different strategies to the context at runtime
5. When `show()` is called, it delegates to the current strategy's `calculateScore()`
6. The context never changes — only the strategy object changes

### Pitfalls and Common Mistakes
- **Public field:** The strategy field should be private with a setter — public fields break encapsulation
- **Client must know strategies:** The client decides which strategy to use, so it must understand the differences
- **Overhead for simple cases:** If you only have 2-3 algorithms that never change, a simple if/else may be clearer

### Connection to Other Patterns
- **State** has identical structure but different intent — State transitions are automatic; Strategy is chosen by the client
- **Template Method** uses inheritance for algorithm variation; Strategy uses composition
- **Command** encapsulates a request; Strategy encapsulates an algorithm

---

## Strategy — Payment

**GoF Category:** Behavioral

![Strategy Payment Diagram](02_Strategy_Payment/Payment/Diagram.jpg)

### Intent
Same pattern as above but demonstrates the interface-based approach (vs abstract class). Shows how Strategy enables open/closed principle — new payment methods can be added without modifying the shopping cart.

### When to Use
- Payment processing with multiple providers (Stripe, PayPal, Apple Pay)
- Shipping calculation (ground, express, overnight)
- Authentication strategies (OAuth, LDAP, local)

### Key Participants
| Class | Role |
|-------|------|
| `Payment` | Strategy interface |
| `CreditCardAlgorithm`, `PaypalAgorithm` | Concrete Strategies |
| `ShoppingCart` | Context |
| `Product` | Domain model |

### Complete Source Code

```java
package com.kejeiri.java.course.controller;

// Strategy interface — defines what all payment methods must do
public interface Payment {
    public void pay(int amount);
}
```

```java
package com.kejeiri.java.course.controller;

// Concrete Strategy — credit card payment
public class CreditCardAlgorithm implements Payment{
    private String name;
    private String cardNumber;

    public CreditCardAlgorithm(String name, String cardNumber) {
        this.name = name;
        this.cardNumber = cardNumber;
    }

    @Override
    public void pay(int amount) {
        System.out.println(amount + " paid with credit card!");
    }
}
```

```java
package com.kejeiri.java.course.controller;

// Concrete Strategy — PayPal payment
public class PaypalAgorithm implements Payment{
    private String email;
    private String password;

    public PaypalAgorithm(String email, String password) {
        this.email = email;
        this.password = password;
    }

    @Override
    public void pay(int amount) {
        System.out.println(amount + " paid with paypal!");
    }
}
```

```java
package com.kejeiri.java.course.controller;
import com.kejeiri.java.course.model.Product;
import java.util.ArrayList;
import java.util.List;

// Context — accepts any Payment strategy at the point of payment
public class ShoppingCart {
    List<Product> productsList;

    public ShoppingCart() { this.productsList = new ArrayList<>(); }
    public void addProduct(Product product){ productsList.add(product); }
    public void removeProduct(Product product){ productsList.remove(product); }

    public int calculateTotal(){
        int sum = 0;
        for (Product product: productsList) { sum += product.getPrice(); }
        return sum;
    }

    // Strategy is passed as a parameter — maximum flexibility
    public void pay(Payment payment){
        int amount = calculateTotal();
        payment.pay(amount);  // Delegate to the strategy
    }
}
```

```java
package com.kejeiri.java.course.model;

public class Product {
    private String upcCode;
    private int price;

    public String getUpcCode() { return upcCode; }
    public void setUpcCode(String upcCode) { this.upcCode = upcCode; }
    public int getPrice() { return price; }
    public Product() { }
    public Product(String upcCode, int price) {
        this.upcCode = upcCode;
        this.price = price;
    }
}
```

```java
package com.kejeiri.java.course;
import com.kejeiri.java.course.controller.CreditCardAlgorithm;
import com.kejeiri.java.course.controller.PaypalAgorithm;
import com.kejeiri.java.course.controller.ShoppingCart;
import com.kejeiri.java.course.model.Product;

public class Main {
    public static void main(String[] args) {
        ShoppingCart cart = new ShoppingCart();
        cart.addProduct(new Product("234", 25));
        cart.addProduct(new Product("987", 15));

        // Same cart, different payment strategies
        cart.pay(new CreditCardAlgorithm("Nocard", "1245454"));  // 40 paid with credit card!
        cart.pay(new PaypalAgorithm("mypaypal@paypal.com", "paypalsucks"));  // 40 paid with paypal!
    }
}
```

### How It Works — Step by Step
1. `Payment` interface defines a single method `pay(int amount)`
2. Each payment provider implements the interface with its own logic and credentials
3. `ShoppingCart` accepts any `Payment` implementation as a method parameter
4. The cart calculates the total and delegates payment to the strategy
5. Adding a new payment method (Bitcoin, Apple Pay) requires zero changes to `ShoppingCart`

### Pitfalls and Common Mistakes
- **Strategy as method parameter vs field:** This example passes strategy as a parameter (good for one-shot operations). Use a field when the strategy is used repeatedly
- **Stateful strategies:** If strategies hold state (like credentials), be careful about thread safety

### Connection to Other Patterns
- This is the **interface-based** variant; pattern 01 uses an **abstract class** — prefer interfaces for flexibility
- In modern Java, simple strategies can be replaced with **lambdas**: `cart.pay(amount -> System.out.println(amount + " paid"))`

---

## Observer — Email (Pull Model)

**GoF Category:** Behavioral

![Observer Diagram](03_Observer_email/Observer/Diagram.jpg)
![Observer Figure](03_Observer_email/Observer/figure.jpg)

### Intent
Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically. The pull model means observers are notified something changed, then they pull the data they need.

### When to Use
- Event handling systems (GUI button clicks, DOM events)
- Publish/subscribe messaging
- Model-View synchronization (MVC)
- Stock price tickers, social media feeds, email notifications

### Key Participants
| Class | Role |
|-------|------|
| `Subject` | Observable interface — manages observer list |
| `Observer` | Observer interface — receives notifications |
| `EmailTopic` | Concrete Subject — posts messages and notifies |
| `EmailTopicSubscriber` | Concrete Observer — pulls updates from subject |

### Complete Source Code

```java
package com.kejeiri.java.course.interfaces;

// Subject (Observable) interface
public interface Subject {
    public void register(Observer observer);
    public void unregister(Observer observer);
    public void notifyObservers();
    public Object getUpdate(Observer observer);  // Pull method — observers call this
}
```

```java
package com.kejeiri.java.course.interfaces;

// Observer interface
public interface Observer {
    public void update();                    // Called by subject to notify
    public void setSubject(Subject subject); // Observer stores reference to subject for pulling
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.interfaces.Observer;
import com.kejeiri.java.course.interfaces.Subject;
import java.util.ArrayList;
import java.util.List;

// Concrete Subject — manages observers and broadcasts changes
public class EmailTopic implements Subject{
    private List<Observer> observers;
    private String message;

    public EmailTopic() { this.observers = new ArrayList<>(); }

    @Override
    public void register(Observer observer) {
        if (observer == null) throw new NullPointerException("Null object/Observer");
        if(!observers.contains(observer)) observers.add(observer);
    }

    @Override
    public void unregister(Observer observer) { observers.remove(observer); }

    @Override
    public void notifyObservers() {
        // Notify all — each observer then pulls what it needs
        for (Observer observer: observers) { observer.update(); }
    }

    @Override
    public Object getUpdate(Observer observer) { return this.message; }

    public void postMessage(String msg){
        System.out.println("Message posted to my Topic " + msg);
        this.message = msg;
        notifyObservers();  // Trigger notification cascade
    }
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.interfaces.Observer;
import com.kejeiri.java.course.interfaces.Subject;

// Concrete Observer — pulls data from subject when notified
public class EmailTopicSubscriber implements Observer {
    private String name;
    private Subject topic;  // Reference to subject for pulling

    public EmailTopicSubscriber(String name) { this.name = name; }

    @Override
    public void update() {
        // PULL: observer actively retrieves data from the subject
        String msg = (String) topic.getUpdate(this);
        if (msg == null) System.out.println(name + " No new message on this topic");
        else System.out.println(name + " Retrieving message: " + msg);
    }

    @Override
    public void setSubject(Subject subject) { this.topic = subject; }
}
```

```java
package com.kejeiri.java.course;
import com.kejeiri.java.course.interfaces.Observer;
import com.kejeiri.java.course.model.EmailTopic;
import com.kejeiri.java.course.model.EmailTopicSubscriber;

public class Main {
    public static void main(String[] args) {
        EmailTopic topic = new EmailTopic();

        Observer firstObserver = new EmailTopicSubscriber("First observer");
        Observer secondObserver = new EmailTopicSubscriber("Second observer");
        Observer thirdObserver = new EmailTopicSubscriber("Third observer");

        // Register observers with the subject
        topic.register(firstObserver);
        topic.register(secondObserver);
        topic.register(thirdObserver);

        // Observers store reference to subject (for pulling)
        firstObserver.setSubject(topic);
        secondObserver.setSubject(topic);
        thirdObserver.setSubject(topic);

        // Manual pull before any message — returns null
        firstObserver.update();
        secondObserver.update();
        thirdObserver.update();

        // Unregister one observer
        topic.unregister(firstObserver);

        // Post message — triggers automatic notification to remaining observers
        topic.postMessage("hello Subscribers");
    }
}
```

### How It Works — Step by Step
1. `EmailTopic` maintains a list of registered `Observer` instances
2. Observers register themselves and store a back-reference to the subject
3. When `postMessage()` is called, the subject stores the message and calls `notifyObservers()`
4. Each observer's `update()` is called — the observer then PULLS data via `topic.getUpdate(this)`
5. Unregistered observers don't receive notifications

### Pitfalls and Common Mistakes
- **Memory leaks:** Forgetting to unregister observers keeps them alive (common in GUI frameworks)
- **Notification order:** Don't depend on the order observers are notified
- **Cascading updates:** Observer A's update triggers a change that notifies Observer B, which triggers... infinite loop
- **Thread safety:** The observer list must be synchronized in concurrent environments, or use `CopyOnWriteArrayList`

### Connection to Other Patterns
- **Mediator** centralizes communication; Observer is decentralized (subject doesn't know what observers do)
- **Event Bus / Pub-Sub** is a more decoupled evolution of Observer
- Java's built-in `java.util.Observable` is deprecated since Java 9 — use `PropertyChangeListener` or reactive libraries

---

## Observer — Broadcast (Push Model)

**GoF Category:** Behavioral

![Observer Broadcast Figure](04_observerBroadcast/radioBroadcast/figure.jpg)

### Intent
Same Observer pattern but using a push model — the subject pushes the relevant data directly to observers during notification. Observers don't need a back-reference to the subject.

### When to Use
- When observers need all the data immediately upon notification
- When you want simpler observer implementations (no need to pull)
- Real-time broadcasting: chat messages, live scores, stock tickers

### Key Participants
| Class | Role |
|-------|------|
| `ITopic` | Subject interface with push-based dispatch |
| `IObserver` | Observer interface receiving pushed data |
| `BreakingNews`, `NewsBulletin` | Concrete Subjects |
| `CustomerSubscriber` | Concrete Observer |

### Complete Source Code

```java
package com.kejeiri.java.course.interfaces;

// Subject interface — push model
public interface ITopic {
    public void register(IObserver observer);
    public void unregister(IObserver observer);
    public void dispatchTo(IObserver observer);  // Push data to a single observer
    public void notifyAllObservers();
}
```

```java
package com.kejeiri.java.course.interfaces;

// Observer interface — receives pushed data
public interface IObserver {
    void attachTo(ITopic topic);       // Lifecycle: attached to a topic
    void deattach();                   // Lifecycle: detached from topic
    void newTopic(String message);     // PUSH: receives data directly
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.interfaces.IObserver;
import com.kejeiri.java.course.interfaces.ITopic;
import java.util.ArrayList;
import java.util.List;

// Concrete Subject — breaking news broadcaster
public class BreakingNews implements ITopic {
    private String message;
    List<IObserver> subscribers;

    public BreakingNews() { this.subscribers = new ArrayList<>(); }

    @Override
    public void register(IObserver observer) {
        if (observer == null) throw new NullPointerException("Subscriber is null");
        if(!subscribers.contains(observer)) {
            observer.attachTo(this);  // Notify observer of attachment
            subscribers.add(observer);
        }
    }

    @Override
    public void unregister(IObserver observer) {
        observer.deattach();  // Notify observer of detachment
        subscribers.remove(observer);
    }

    @Override
    public void dispatchTo(IObserver observer) {
        observer.newTopic(message);  // PUSH: send data directly to observer
    }

    @Override
    public void notifyAllObservers() {
        for (IObserver observer : this.subscribers) { dispatchTo(observer); }
    }

    public void broadcastBreakingNews(String message){
        this.message = message;
        notifyAllObservers();
    }
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.interfaces.IObserver;
import com.kejeiri.java.course.interfaces.ITopic;
import java.util.ArrayList;
import java.util.List;

// Concrete Subject — news bulletin broadcaster
public class NewsBulletin implements ITopic {
    List<IObserver> listeners;
    private String message;

    public NewsBulletin() { this.listeners = new ArrayList<>(); }

    @Override
    public void register(IObserver observer) {
        if (observer == null) throw new NullPointerException("Observer is null!");
        else if (!listeners.contains(observer)) {
            observer.attachTo(this);
            listeners.add(observer);
        }
    }

    @Override
    public void unregister(IObserver observer) {
        observer.deattach();
        listeners.remove(observer);
    }

    @Override
    public void dispatchTo(IObserver observer) { observer.newTopic(message); }

    @Override
    public void notifyAllObservers() {
        for (IObserver observer : this.listeners) { dispatchTo(observer); }
    }

    public void postNews(String message){
        this.message = message;
        notifyAllObservers();
    }
}
```

```java
package com.kejeiri.java.course.model;
import com.kejeiri.java.course.interfaces.IObserver;
import com.kejeiri.java.course.interfaces.ITopic;

// Concrete Observer — receives pushed messages
public class CustomerSubscriber implements IObserver {
    private String name;
    private ITopic topic;

    public CustomerSubscriber(String name) { this.name = name; }

    @Override
    public void attachTo(ITopic topic) { this.topic = topic; }

    @Override
    public void deattach() { this.topic = null; }

    @Override
    public void newTopic(String message) {
        // Data is PUSHED — no need to pull from subject
        System.out.println("the topic: " + message + " for " + name + " has been broadcast!");
    }
}
```

```java
package com.kejeiri.java.course;
import com.kejeiri.java.course.interfaces.IObserver;
import com.kejeiri.java.course.model.BreakingNews;
import com.kejeiri.java.course.model.CustomerSubscriber;
import com.kejeiri.java.course.model.NewsBulletin;

public class Main {
    public static void main(String[] args) {
        // News Bulletin demo
        NewsBulletin news = new NewsBulletin();
        IObserver sub1 = new CustomerSubscriber("Subscription Customer 1");
        IObserver sub2 = new CustomerSubscriber("Subscription Customer 2");
        IObserver sub3 = new CustomerSubscriber("Subscription Customer 3");
        IObserver sub4 = new CustomerSubscriber("Subscription Customer 4");
        news.register(sub1);
        news.register(sub2);
        news.register(sub3);
        news.register(sub4);
        news.postNews("All subscriptions included");
        news.unregister(sub3);
        news.postNews("one Customer subscription's been cancelled");

        // Breaking News demo
        BreakingNews breakingNews = new BreakingNews();
        IObserver obs1 = new CustomerSubscriber("Customer observer 1");
        IObserver obs2 = new CustomerSubscriber("Customer observer 2");
        breakingNews.register(obs1);
        breakingNews.register(obs2);
        breakingNews.broadcastBreakingNews("Breaking news 1");
        breakingNews.unregister(obs2);
        breakingNews.broadcastBreakingNews("Breaking news 2");
    }
}
```

### How It Works — Step by Step
1. Subject stores the message and calls `notifyAllObservers()`
2. For each observer, `dispatchTo(observer)` is called
3. `dispatchTo()` calls `observer.newTopic(message)` — pushing the data directly
4. The observer receives the message as a parameter — no need to call back to the subject
5. Pull model: "something changed, come get it" vs Push model: "here's what changed"

### Pitfalls and Common Mistakes
- **Push too much data:** If you push everything, observers receive data they don't need — wasteful
- **Push too little:** If you push only a notification, observers need to pull anyway — defeating the purpose
- **Balance:** Push the most commonly needed data; let observers pull for extras

### Connection to Other Patterns
- Pull model (pattern 03) gives observers more control over what data they retrieve
- Push model (this pattern) is simpler for observers but couples them to the data format
- Modern frameworks (RxJava, Project Reactor) use push-based reactive streams


---

## Command

**GoF Category:** Behavioral

![Command Diagram](11_CommandPattern/CommandPattern/Diagram.jpg)

### Intent
Encapsulates a request as an object, thereby letting you parameterize clients with different requests, queue or log requests, and support undoable operations. Decouples the object that invokes the operation from the one that knows how to perform it.

### When to Use
- Undo/redo functionality (text editors, drawing apps)
- Macro recording — store a sequence of commands for replay
- Task queues and job scheduling
- GUI buttons/menu items that trigger actions
- Transaction logging for crash recovery

### Key Participants
| Class | Role |
|-------|------|
| `Command` | Interface declaring `execute()` |
| Concrete Commands | Encapsulate a receiver and an action |
| `Invoker` | Asks the command to carry out the request |
| `Receiver` | Knows how to perform the actual work |

### Complete Source Code
*(Pattern 11 in the repo)*

```java
// Command interface
public interface Command {
    void execute();
}

// Receiver — knows how to perform the actual operations
public class Light {
    public void turnOn() { System.out.println("Light is ON"); }
    public void turnOff() { System.out.println("Light is OFF"); }
}

// Concrete Command — encapsulates "turn on" action
public class LightOnCommand implements Command {
    private Light light;  // Reference to receiver

    public LightOnCommand(Light light) { this.light = light; }

    @Override
    public void execute() {
        light.turnOn();  // Delegates to receiver
    }
}

// Concrete Command — encapsulates "turn off" action
public class LightOffCommand implements Command {
    private Light light;

    public LightOffCommand(Light light) { this.light = light; }

    @Override
    public void execute() {
        light.turnOff();
    }
}

// Invoker — triggers commands without knowing what they do
public class RemoteControl {
    private Command command;

    public void setCommand(Command command) { this.command = command; }

    public void pressButton() {
        command.execute();  // Invoker doesn't know what happens — just executes
    }
}

// Client — wires everything together
public class Main {
    public static void main(String[] args) {
        Light light = new Light();                    // Receiver
        Command lightOn = new LightOnCommand(light); // Command wraps receiver+action
        Command lightOff = new LightOffCommand(light);

        RemoteControl remote = new RemoteControl();  // Invoker
        remote.setCommand(lightOn);
        remote.pressButton();  // Light is ON

        remote.setCommand(lightOff);
        remote.pressButton();  // Light is OFF
    }
}
```

### How It Works — Step by Step
1. `Light` (receiver) has the actual business logic: `turnOn()`, `turnOff()`
2. `LightOnCommand` wraps the receiver and binds it to a specific action
3. `RemoteControl` (invoker) holds a command reference — it doesn't know about Light
4. When `pressButton()` is called, the invoker calls `command.execute()`
5. The command delegates to the receiver's method
6. To add undo: store previous commands in a stack, add an `undo()` method to Command

### Pitfalls and Common Mistakes
- **Too many command classes:** Each action becomes a class — can lead to class explosion. Use lambdas for simple commands
- **Forgetting undo state:** For undo to work, commands must store enough state to reverse the action
- **Command vs Strategy confusion:** Both encapsulate behavior, but Command encapsulates a request (what to do + who to do it to); Strategy encapsulates an algorithm (how to do something)

### Connection to Other Patterns
- **Memento** can store state for undo operations within commands
- **Composite** can create macro commands (a command that executes a list of commands)
- **Strategy** encapsulates algorithms; **Command** encapsulates requests
- **Chain of Responsibility** passes a request along a chain; Command binds a request to a specific handler

---

## Template Method

**GoF Category:** Behavioral

![Template Diagram 1](14_TemplatePattern/TemplatePattern/Diagram1.jpg)
![Template Diagram 2](14_TemplatePattern/TemplatePattern/Diagram2.jpg)

### Intent
Defines the skeleton of an algorithm in a base class, letting subclasses override specific steps without changing the algorithm's structure. The base class controls the workflow; subclasses provide the details.

### When to Use
- When multiple classes share the same algorithm structure but differ in specific steps
- Framework hooks — the framework defines the workflow, plugins fill in the details
- Data processing pipelines (read → transform → write) where transform varies
- Game loops, build processes, report generation

### Key Participants
| Class | Role |
|-------|------|
| Abstract Class | Defines the template method (final) and abstract/hook steps |
| Concrete Classes | Override the abstract steps with specific implementations |

### Complete Source Code
*(Pattern 14 in the repo)*

```java
// Abstract class with template method
public abstract class DataMiner {

    // Template method — defines the algorithm skeleton
    // Should be final to prevent subclasses from changing the structure
    public final void mine() {
        openFile();
        extractData();
        parseData();
        analyzeData();
        sendReport();
        closeFile();
    }

    // Steps that vary — subclasses must implement
    abstract void openFile();
    abstract void extractData();
    abstract void parseData();
    abstract void closeFile();

    // Steps with default behavior — subclasses CAN override (hooks)
    void analyzeData() {
        System.out.println("Analyzing data...");
    }

    void sendReport() {
        System.out.println("Sending report via email...");
    }
}

// Concrete implementation for CSV files
public class CSVDataMiner extends DataMiner {
    @Override
    void openFile() { System.out.println("Opening CSV file..."); }

    @Override
    void extractData() { System.out.println("Extracting data from CSV..."); }

    @Override
    void parseData() { System.out.println("Parsing CSV rows..."); }

    @Override
    void closeFile() { System.out.println("Closing CSV file..."); }
}

// Concrete implementation for PDF files
public class PDFDataMiner extends DataMiner {
    @Override
    void openFile() { System.out.println("Opening PDF file..."); }

    @Override
    void extractData() { System.out.println("Extracting text from PDF..."); }

    @Override
    void parseData() { System.out.println("Parsing PDF content..."); }

    @Override
    void closeFile() { System.out.println("Closing PDF file..."); }
}

public class Main {
    public static void main(String[] args) {
        DataMiner csvMiner = new CSVDataMiner();
        csvMiner.mine();  // Runs the full algorithm with CSV-specific steps

        DataMiner pdfMiner = new PDFDataMiner();
        pdfMiner.mine();  // Same algorithm, PDF-specific steps
    }
}
```

### How It Works — Step by Step
1. `DataMiner` defines `mine()` as the template method — it calls steps in a fixed order
2. Abstract methods (`openFile`, `extractData`, etc.) MUST be implemented by subclasses
3. Hook methods (`analyzeData`, `sendReport`) have defaults that CAN be overridden
4. `CSVDataMiner` and `PDFDataMiner` provide their own implementations of the abstract steps
5. The algorithm structure (open → extract → parse → analyze → report → close) never changes
6. Making `mine()` final prevents subclasses from altering the workflow

### Pitfalls and Common Mistakes
- **Forgetting to make template method final:** Subclasses could override the entire algorithm, defeating the purpose
- **Too many abstract methods:** If subclasses must implement 10+ methods, the template is too granular
- **Fragile base class:** Changes to the base class algorithm affect all subclasses

### Connection to Other Patterns
- **Strategy** uses composition to vary the entire algorithm; **Template Method** uses inheritance to vary steps
- **Factory Method** is often called from within a Template Method
- The `Hamburger.prepare()/cook()/box()` in the Factory pattern is actually a Template Method

---

## Iterator

**GoF Category:** Behavioral

![Iterator Diagram](15_IteratorPattern/IteratorPattern/Diagram.jpg)
![Iterator Figure](15_IteratorPattern/IteratorPattern/figure.jpg)

### Intent
Provides a way to access elements of a collection sequentially without exposing its underlying representation. Decouples traversal logic from the collection, allowing multiple traversal strategies.

### When to Use
- When you need to traverse a collection without exposing its internal structure
- When you want multiple simultaneous traversals of the same collection
- When you want a uniform interface for traversing different collection types
- Custom data structures (trees, graphs) that need standard iteration

### Key Participants
| Class | Role |
|-------|------|
| `Iterator` | Interface defining traversal operations (hasNext, next) |
| `Aggregate/Collection` | Interface for creating iterators |
| Concrete Iterator | Implements traversal for a specific collection |
| Concrete Collection | Implements the collection and creates its iterator |

### Complete Source Code
*(Pattern 15 in the repo)*

```java
// Iterator interface
public interface Iterator<T> {
    boolean hasNext();
    T next();
}

// Collection interface
public interface Container<T> {
    Iterator<T> getIterator();
}

// Concrete collection with internal iterator
public class NameRepository implements Container<String> {
    private String[] names = {"John", "Jane", "Jack", "Jill"};

    @Override
    public Iterator<String> getIterator() {
        return new NameIterator();  // Factory method for iterator
    }

    // Inner class — has access to the collection's internal state
    private class NameIterator implements Iterator<String> {
        int index = 0;

        @Override
        public boolean hasNext() {
            return index < names.length;
        }

        @Override
        public String next() {
            if (hasNext()) {
                return names[index++];
            }
            return null;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        NameRepository repository = new NameRepository();
        Iterator<String> iterator = repository.getIterator();

        while (iterator.hasNext()) {
            String name = iterator.next();
            System.out.println("Name: " + name);
        }
    }
}
```

### How It Works — Step by Step
1. `Container` declares `getIterator()` — the factory method for creating iterators
2. `NameRepository` stores names in an array and implements `getIterator()`
3. `NameIterator` is a private inner class — it has access to the `names` array
4. It tracks position with an `index` field, advancing on each `next()` call
5. The client uses only `hasNext()` and `next()` — doesn't know it's an array internally
6. The collection could switch to a LinkedList internally without affecting clients

### Pitfalls and Common Mistakes
- **ConcurrentModificationException:** Modifying a collection while iterating causes issues. Use `CopyOnWriteArrayList` or iterator's `remove()` method
- **Reinventing the wheel:** Java's `java.util.Iterator` and enhanced for-loop already provide this. Only implement custom iterators for custom data structures
- **Stateful iterators:** Each iterator instance maintains its own position — don't share iterators between threads

### Connection to Other Patterns
- **Composite** often uses Iterator to traverse tree structures
- **Factory Method** is used to create the appropriate iterator
- **Visitor** can be used with Iterator to perform operations on each element
- Java's `Iterable`/`Iterator` interfaces and the enhanced for-loop are the standard implementation


---

## State — Procedural (Anti-pattern)

**GoF Category:** Behavioral

![State Diagram 1](16_StatePattern/StatePattern/Diagram1.jpg)
![State Diagram 2](16_StatePattern/StatePattern/Diagram2.jpg)
![State Figure](16_StatePattern/StatePattern/figure.jpg)

### Intent
Demonstrates the WRONG way to handle state — using conditionals (if/else or switch) to check state before every action. This is the "before" that motivates the State pattern. Shown here as a contrast to the proper OO solution.

### When to Use
- **Don't use this approach.** It's shown as the anti-pattern that the State pattern solves.
- Acceptable only for trivial state machines with 2-3 states that will never grow.

### Key Participants
| Class | Role |
|-------|------|
| `SodaVendingMachine` | Monolithic class with state constants and conditional logic |

### Complete Source Code
*(Pattern 16 in the repo — the problem)*

```java
package com.java.course;

// Anti-pattern: all state logic in one class with conditionals
public class SodaVendingMachine {
    // States as integer constants
    final static int SOLD_OUT = 0;
    final static int NO_MONEY = 1;
    final static int HAS_MONEY = 2;
    final static int SOLD = 3;

    int state = SOLD_OUT;
    int count = 0;

    public SodaVendingMachine(int count) {
        this.count = count;
        if (count > 0) state = NO_MONEY;
    }

    // Every method has a switch/if for EVERY state — violates Open/Closed Principle
    public void insertMoney() {
        if (state == HAS_MONEY) {
            System.out.println("No need to insert another dollar");
        } else if (state == NO_MONEY) {
            state = HAS_MONEY;
            System.out.println("You inserted a dollar");
        } else if (state == SOLD_OUT) {
            System.out.println("Machine sold out, can't insert money");
        } else if (state == SOLD) {
            System.out.println("Please wait, soda coming");
        }
    }

    public void ejectMoney() {
        if (state == HAS_MONEY) {
            System.out.println("Returning money");
            state = NO_MONEY;
        } else if (state == NO_MONEY) {
            System.out.println("You haven't inserted money");
        } else if (state == SOLD) {
            System.out.println("Sorry, already selected");
        } else if (state == SOLD_OUT) {
            System.out.println("Can't eject, machine sold out");
        }
    }

    public void select() {
        if (state == HAS_MONEY) {
            System.out.println("Selected...");
            state = SOLD;
        } else if (state == NO_MONEY) {
            System.out.println("Insert money first");
        } else if (state == SOLD) {
            System.out.println("Already dispensing");
        } else if (state == SOLD_OUT) {
            System.out.println("Sold out");
        }
    }

    public void dispense() {
        if (state == SOLD) {
            System.out.println("Dispensing soda");
            count--;
            if (count == 0) state = SOLD_OUT;
            else state = NO_MONEY;
        } else {
            System.out.println("Need to pay first");
        }
    }
}
```

### Problems with This Approach
1. **Open/Closed violation:** Adding a new state requires modifying EVERY method
2. **Scattered logic:** State behavior is spread across all methods instead of being cohesive
3. **Error-prone:** Easy to forget a state case in one of the methods
4. **Hard to test:** Can't test one state in isolation
5. **Doesn't scale:** With 10 states and 5 methods, you have 50 conditional branches

---

## State — Object-Oriented

**GoF Category:** Behavioral

![State OO Diagram 1](17_StatePatternSolution/StatePatternSolution/Diagram1.jpg)
![State OO Diagram 2](17_StatePatternSolution/StatePatternSolution/Diagram2.jpg)
![State OO Figure](17_StatePatternSolution/StatePatternSolution/figure.jpg)

### Intent
Allows an object to alter its behavior when its internal state changes. The object will appear to change its class. Each state is encapsulated in its own class, and the context delegates behavior to the current state object.

### When to Use
- When an object's behavior depends on its state and must change at runtime
- When operations have large conditional statements that depend on state
- Vending machines, TCP connections, document workflows (draft → review → published)
- Game character states (idle, running, jumping, attacking)

### Key Participants
| Class | Role |
|-------|------|
| `IState` | State interface — declares behavior for each action |
| `HasMoneyState`, `NoMoneyState`, `SoldState`, `SoldOutState` | Concrete States |
| `SodaVendingMachine` | Context — delegates to current state, provides state transition methods |

### Complete Source Code

```java
package com.java.course.model;

// State interface — each state handles all possible actions
public interface IState {
    void insertMoney();
    void ejectMoney();
    void select();
    void dispense();
}
```

```java
package com.java.course.model;

// Context — delegates all behavior to the current state object
public class SodaVendingMachine {
    private IState soldOutState;
    private IState noMoneyState;
    private IState hasMoneyState;
    private IState soldState;
    private IState state = soldOutState;  // Current state
    private int count = 0;

    public SodaVendingMachine(int numberOfSodas) {
        // Create all state objects, passing context reference
        this.hasMoneyState = new HasMoneyState(this);
        this.noMoneyState = new NoMoneyState(this);
        this.soldOutState = new SoldOutState(this);
        this.soldState = new SoldState(this);
        this.count = numberOfSodas;
        if (numberOfSodas > 0) { state = noMoneyState; }
    }

    // Delegate all actions to current state
    public void insertMoney() { state.insertMoney(); }
    public void ejectMoney() { state.ejectMoney(); }
    public void select() { state.select(); }
    public void dispense() { state.dispense(); }

    // State objects use these to trigger transitions
    public IState getSoldOutState() { return soldOutState; }
    public IState getNoMoneyState() { return noMoneyState; }
    public IState getHasMoneyState() { return hasMoneyState; }
    public IState getSoldState() { return soldState; }
    public IState getState() { return state; }
    public void setState(IState state) { this.state = state; }
    public void setCount(int count) { this.count = count; }
    public int getCount() { return count; }
}
```

```java
package com.java.course.model;

// Concrete State: machine has money inserted
public class HasMoneyState implements IState{
    private SodaVendingMachine sodaVendingMachine;

    public HasMoneyState(SodaVendingMachine sodaVendingMachine) {
        this.sodaVendingMachine = sodaVendingMachine;
    }

    @Override
    public void insertMoney() {
        System.out.println("No need to insert a dollar");
    }

    @Override
    public void ejectMoney() {
        System.out.println("Returning a dollar");
        // Transition to NoMoney state
        sodaVendingMachine.setState(sodaVendingMachine.getNoMoneyState());
    }

    @Override
    public void select() {
        System.out.println("selected item...");
        // Transition to Sold state
        sodaVendingMachine.setState(sodaVendingMachine.getSoldState());
        sodaVendingMachine.setCount(sodaVendingMachine.getCount() - 1);
    }

    @Override
    public void dispense() {
        System.out.println("No soda dispensed...");
    }
}
```

```java
package com.java.course.model;

// Concrete State: no money in machine
public class NoMoneyState implements IState{
    private SodaVendingMachine sodaVendingMachine;

    public NoMoneyState(SodaVendingMachine sodaVendingMachine) {
        this.sodaVendingMachine = sodaVendingMachine;
    }

    @Override
    public void insertMoney() {
        System.out.println("You inserted a dollar");
        // Transition to HasMoney state
        sodaVendingMachine.setState(sodaVendingMachine.getHasMoneyState());
    }

    @Override
    public void ejectMoney() {
        System.out.println("you haven't inserted a dollar");
    }

    @Override
    public void select() {
        System.out.println("Your selected but there is no money");
    }

    @Override
    public void dispense() {
        System.out.println("Pay me first buddy!");
    }
}
```

```java
package com.java.course.model;

// Concrete State: soda has been sold, dispensing
public class SoldState implements IState {
    private SodaVendingMachine sodaVendingMachine;

    public SoldState(SodaVendingMachine sodaVendingMachine) {
        this.sodaVendingMachine = sodaVendingMachine;
    }

    @Override
    public void insertMoney() {
        System.out.println("give a second soda coming right up");
    }

    @Override
    public void ejectMoney() {
        System.out.println("Nope... you can't eject the money");
    }

    @Override
    public void select() {
        System.out.println("sorry the soda is coming!");
        sodaVendingMachine.setCount(sodaVendingMachine.getCount() - 1);
    }

    @Override
    public void dispense() {
        System.out.println("Stop trying to get a second soda for free");
        // Transition based on remaining inventory
        if (sodaVendingMachine.getCount() > 0) {
            sodaVendingMachine.setState(sodaVendingMachine.getNoMoneyState());
        } else {
            sodaVendingMachine.setState(sodaVendingMachine.getSoldOutState());
        }
    }
}
```

```java
package com.java.course.model;

// Concrete State: machine is sold out
public class SoldOutState implements IState{
    private SodaVendingMachine sodaVendingMachine;

    public SoldOutState(SodaVendingMachine sodaVendingMachine) {
        this.sodaVendingMachine = sodaVendingMachine;
    }

    @Override
    public void insertMoney() { System.out.println("machine sold out"); }

    @Override
    public void ejectMoney() { System.out.println("insert money before ejecting"); }

    @Override
    public void select() { System.out.println("No soda available"); }

    @Override
    public void dispense() { System.out.println("Sold out!"); }
}
```

```java
package com.java.course;
import com.java.course.model.SodaVendingMachine;

public class Main {
    public static void main(String[] args) {
        SodaVendingMachine machine = new SodaVendingMachine(10);

        machine.insertMoney();  // "You inserted a dollar" → transitions to HasMoney
        machine.select();       // "selected item..." → transitions to Sold
        // Machine is now in Sold state, count = 9

        machine.insertMoney();
        machine.select();
        machine.insertMoney();
        machine.select();
        // count = 7
    }
}
```

### How It Works — Step by Step
1. `SodaVendingMachine` creates all state objects in its constructor, passing `this` as context
2. Initial state is set to `noMoneyState` (if sodas available)
3. When `insertMoney()` is called on the machine, it delegates to `state.insertMoney()`
4. `NoMoneyState.insertMoney()` prints a message and transitions: `machine.setState(machine.getHasMoneyState())`
5. Next call to any method on the machine now delegates to `HasMoneyState`
6. Each state class handles only its own behavior — clean separation of concerns
7. Adding a new state (e.g., "WinnerState") means adding one new class — no existing code changes

### Pitfalls and Common Mistakes
- **State explosion:** Too many states with too many transitions becomes hard to manage — consider a state machine library
- **Circular references:** Context holds states, states hold context — be careful with serialization
- **Who triggers transitions?** States trigger their own transitions (as shown), or the context can manage transitions centrally
- **Shared state objects:** If states are stateless, they can be shared (flyweight). If they hold data, each context needs its own state instances

### Connection to Other Patterns
- **Strategy** looks identical structurally but differs in intent: Strategy is chosen by the client; State transitions happen internally
- **State** objects are often **Singletons** or **Flyweights** if they're stateless
- **Mediator** can coordinate state transitions in complex multi-object scenarios


---

## Mediator

**GoF Category:** Behavioral

![Mediator Diagram](23_MediatorDesignPattern/MediatorDesignPattern/Diagram.jpg)
![Mediator Figure 1](23_MediatorDesignPattern/MediatorDesignPattern/figure1.jpg)
![Mediator Figure 2](23_MediatorDesignPattern/MediatorDesignPattern/figure2.jpg)

### Intent
Defines an object that encapsulates how a set of objects interact. Promotes loose coupling by keeping objects from referring to each other explicitly, and lets you vary their interaction independently.

### When to Use
- When a set of objects communicate in complex but well-defined ways
- When reusing an object is difficult because it refers to many other objects
- Chat rooms, air traffic control, UI form validation (fields depend on each other)
- Microservice orchestration, event buses

### Key Participants
| Class | Role |
|-------|------|
| `Mediator` | Interface defining communication methods |
| `ConcreteMediator` | Implements coordination logic between colleagues |
| `Colleague` | Base class for objects that communicate through the mediator |
| Concrete Colleagues | Specific participants that send/receive through mediator |

### Complete Source Code
*(Pattern 23 in the repo)*

```java
// Mediator interface
public interface ChatMediator {
    void sendMessage(String msg, User user);
    void addUser(User user);
}

// Colleague base class
public abstract class User {
    protected ChatMediator mediator;
    protected String name;

    public User(ChatMediator mediator, String name) {
        this.mediator = mediator;
        this.name = name;
    }

    public abstract void send(String msg);
    public abstract void receive(String msg);
}

// Concrete Mediator — coordinates message passing
public class ChatRoom implements ChatMediator {
    private List<User> users = new ArrayList<>();

    @Override
    public void addUser(User user) { users.add(user); }

    @Override
    public void sendMessage(String msg, User sender) {
        // Mediator decides who receives — everyone except sender
        for (User user : users) {
            if (user != sender) {
                user.receive(msg);
            }
        }
    }
}

// Concrete Colleague
public class ChatUser extends User {
    public ChatUser(ChatMediator mediator, String name) {
        super(mediator, name);
    }

    @Override
    public void send(String msg) {
        System.out.println(name + " sends: " + msg);
        mediator.sendMessage(msg, this);  // Communicate through mediator, not directly
    }

    @Override
    public void receive(String msg) {
        System.out.println(name + " receives: " + msg);
    }
}

public class Main {
    public static void main(String[] args) {
        ChatMediator chatRoom = new ChatRoom();

        User john = new ChatUser(chatRoom, "John");
        User jane = new ChatUser(chatRoom, "Jane");
        User jack = new ChatUser(chatRoom, "Jack");

        chatRoom.addUser(john);
        chatRoom.addUser(jane);
        chatRoom.addUser(jack);

        john.send("Hello everyone!");
        // Jane receives: Hello everyone!
        // Jack receives: Hello everyone!
    }
}
```

### How It Works — Step by Step
1. `ChatRoom` (mediator) maintains a list of all users
2. Users don't know about each other — they only know the mediator
3. When John calls `send("Hello")`, it delegates to `mediator.sendMessage("Hello", this)`
4. The mediator iterates all users and calls `receive()` on everyone except the sender
5. Adding new communication rules (e.g., private messages, blocked users) only changes the mediator

### Pitfalls and Common Mistakes
- **God object:** The mediator can become overly complex if it handles too many interactions — split into multiple mediators
- **Single point of failure:** All communication goes through one object
- **Over-use:** Don't use Mediator for simple two-object interactions — direct communication is fine

### Connection to Other Patterns
- **Observer** is distributed notification; **Mediator** is centralized coordination
- **Facade** provides a simplified interface to a subsystem; **Mediator** coordinates peer-to-peer communication
- Often used with **Command** — commands are sent through the mediator

---

## Visitor

**GoF Category:** Behavioral

![Visitor Diagram](24_VisitorDesignPattern/VisitorDesignPattern/Diagram.jpg)
![Visitor Figure](24_VisitorDesignPattern/VisitorDesignPattern/figure1.jpg)

### Intent
Represents an operation to be performed on elements of an object structure. Lets you define a new operation without changing the classes of the elements on which it operates. Uses double dispatch to call the correct method.

### When to Use
- When you need to perform many unrelated operations on a structure of objects
- When the object structure rarely changes but you frequently add new operations
- Compilers (AST traversal), document export (PDF, HTML, XML from same structure)
- Tax calculation, report generation across heterogeneous collections

### Key Participants
| Class | Role |
|-------|------|
| `Visitor` | Interface declaring visit methods for each element type |
| Concrete Visitors | Implement specific operations for each element type |
| `Element` | Interface declaring `accept(Visitor)` |
| Concrete Elements | Call the appropriate visitor method (double dispatch) |

### Complete Source Code
*(Pattern 24 in the repo)*

```java
// Visitor interface — one method per element type
public interface ShoppingCartVisitor {
    int visit(Book book);
    int visit(Fruit fruit);
}

// Element interface
public interface ItemElement {
    int accept(ShoppingCartVisitor visitor);  // Double dispatch entry point
}

// Concrete Element — Book
public class Book implements ItemElement {
    private int price;
    private String isbn;

    public Book(int price, String isbn) {
        this.price = price;
        this.isbn = isbn;
    }

    public int getPrice() { return price; }
    public String getIsbn() { return isbn; }

    @Override
    public int accept(ShoppingCartVisitor visitor) {
        return visitor.visit(this);  // Calls visit(Book) — double dispatch
    }
}

// Concrete Element — Fruit
public class Fruit implements ItemElement {
    private int pricePerKg;
    private int weight;
    private String name;

    public Fruit(int pricePerKg, int weight, String name) {
        this.pricePerKg = pricePerKg;
        this.weight = weight;
        this.name = name;
    }

    public int getPricePerKg() { return pricePerKg; }
    public int getWeight() { return weight; }
    public String getName() { return name; }

    @Override
    public int accept(ShoppingCartVisitor visitor) {
        return visitor.visit(this);  // Calls visit(Fruit) — double dispatch
    }
}

// Concrete Visitor — calculates total price
public class ShoppingCartVisitorImpl implements ShoppingCartVisitor {
    @Override
    public int visit(Book book) {
        int cost = book.getPrice();
        if (cost > 50) cost -= 5;  // Discount for expensive books
        System.out.println("Book ISBN: " + book.getIsbn() + " cost: " + cost);
        return cost;
    }

    @Override
    public int visit(Fruit fruit) {
        int cost = fruit.getPricePerKg() * fruit.getWeight();
        System.out.println(fruit.getName() + " cost: " + cost);
        return cost;
    }
}

public class Main {
    public static void main(String[] args) {
        ItemElement[] items = new ItemElement[]{
            new Book(20, "1234"),
            new Book(100, "5678"),
            new Fruit(10, 2, "Banana"),
            new Fruit(5, 5, "Apple")
        };

        ShoppingCartVisitor visitor = new ShoppingCartVisitorImpl();
        int total = 0;
        for (ItemElement item : items) {
            total += item.accept(visitor);
        }
        System.out.println("Total cost: " + total);
    }
}
```

### How It Works — Step by Step
1. `ItemElement` declares `accept(visitor)` — the entry point for double dispatch
2. `Book.accept(visitor)` calls `visitor.visit(this)` — the compiler resolves to `visit(Book)`
3. `Fruit.accept(visitor)` calls `visitor.visit(this)` — resolves to `visit(Fruit)`
4. The visitor's `visit(Book)` method contains Book-specific logic (discount calculation)
5. The visitor's `visit(Fruit)` method contains Fruit-specific logic (weight × price)
6. To add a new operation (e.g., tax calculation), create a new Visitor — no element changes needed

### Why Double Dispatch?
Java uses single dispatch — the method called depends only on the receiver's runtime type. Visitor achieves double dispatch:
- First dispatch: `item.accept(visitor)` — dispatches on item's type
- Second dispatch: `visitor.visit(this)` — dispatches on visitor's type

### Pitfalls and Common Mistakes
- **Adding new element types is hard:** Every visitor must be updated with a new `visit()` method — violates Open/Closed for elements
- **Breaking encapsulation:** Visitors often need access to element internals (getters)
- **Complexity:** Double dispatch is confusing for developers unfamiliar with the pattern

### Connection to Other Patterns
- **Composite** + **Visitor** is a powerful combination for tree operations
- **Iterator** traverses; **Visitor** operates on each element during traversal
- **Strategy** varies one algorithm; **Visitor** varies operations across a type hierarchy

---

## Memento

**GoF Category:** Behavioral

![Memento Diagram](25_MementoDesignPattern/MementoDesignPattern/Diagram.jpg)
![Memento Figure](25_MementoDesignPattern/MementoDesignPattern/figure1.jpg)

### Intent
Captures and externalizes an object's internal state without violating encapsulation, so the object can be restored to this state later. Enables undo/redo functionality.

### When to Use
- Undo/redo in editors (text, graphics, code)
- Saving game state (checkpoints, save slots)
- Transaction rollback in databases
- Browser back button (page state history)

### Key Participants
| Class | Role |
|-------|------|
| `Originator` | The object whose state needs saving — creates and restores from mementos |
| `Memento` | Stores the originator's internal state (opaque to others) |
| `Caretaker` | Manages memento lifecycle (stores, retrieves) without examining contents |

### Complete Source Code
*(Pattern 25 in the repo)*

```java
// Memento — stores state snapshot (should be immutable)
public class Memento {
    private final String state;

    public Memento(String state) { this.state = state; }

    public String getState() { return state; }
}

// Originator — the object whose state we want to save/restore
public class Editor {
    private String content;

    public void setContent(String content) { this.content = content; }
    public String getContent() { return content; }

    // Creates a memento containing current state
    public Memento save() {
        return new Memento(content);
    }

    // Restores state from a memento
    public void restore(Memento memento) {
        content = memento.getState();
    }
}

// Caretaker — manages the history of mementos
public class History {
    private List<Memento> mementos = new ArrayList<>();

    public void push(Memento memento) { mementos.add(memento); }

    public Memento pop() {
        if (mementos.isEmpty()) return null;
        Memento last = mementos.get(mementos.size() - 1);
        mementos.remove(mementos.size() - 1);
        return last;
    }
}

public class Main {
    public static void main(String[] args) {
        Editor editor = new Editor();
        History history = new History();

        editor.setContent("Version 1");
        history.push(editor.save());  // Save state

        editor.setContent("Version 2");
        history.push(editor.save());  // Save state

        editor.setContent("Version 3");
        System.out.println(editor.getContent());  // "Version 3"

        // Undo — restore previous state
        editor.restore(history.pop());
        System.out.println(editor.getContent());  // "Version 2"

        editor.restore(history.pop());
        System.out.println(editor.getContent());  // "Version 1"
    }
}
```

### How It Works — Step by Step
1. `Editor` (originator) has internal state (`content`) that changes over time
2. Before making changes, the client calls `editor.save()` which creates a `Memento` snapshot
3. The `History` (caretaker) stores mementos in a list — it never looks inside them
4. To undo, the client pops a memento from history and calls `editor.restore(memento)`
5. The editor's state is rolled back to the saved snapshot
6. Encapsulation is preserved — only the Editor knows how to create/restore from mementos

### Pitfalls and Common Mistakes
- **Memory consumption:** Storing full state snapshots for every change is expensive. Use incremental/delta mementos for large objects
- **Deep copy required:** If the originator's state contains mutable objects, the memento must deep-copy them
- **Caretaker lifetime:** Mementos must be garbage-collected when no longer needed

### Connection to Other Patterns
- **Command** + **Memento** = undo system. Command stores the action; Memento stores the state before the action
- **Prototype** can be used to implement memento (clone the originator)
- **Iterator** over a history of mementos enables undo/redo navigation

---

## Interpreter

**GoF Category:** Behavioral

![Interpreter Diagram](26_InterpreterDesignPattern/InterpreterDesignPattern/Diagram.jpg)
![Interpreter Figure](26_InterpreterDesignPattern/InterpreterDesignPattern/figure1.jpg)

### Intent
Defines a representation for a grammar along with an interpreter that uses the representation to interpret sentences in the language. Each grammar rule becomes a class.

### When to Use
- Simple domain-specific languages (DSLs)
- Mathematical expression evaluation
- SQL parsing, regex engines, configuration file parsing
- Rule engines for business logic

### Key Participants
| Class | Role |
|-------|------|
| `Expression` | Abstract expression interface |
| `TerminalExpression` | Interprets terminal symbols (literals, variables) |
| `NonTerminalExpression` | Interprets grammar rules (AND, OR, PLUS) |
| `Context` | Contains information global to the interpreter |

### Complete Source Code
*(Pattern 26 in the repo)*

```java
// Abstract Expression
public interface Expression {
    boolean interpret(String context);
}

// Terminal Expression — checks if a word exists in context
public class TerminalExpression implements Expression {
    private String data;

    public TerminalExpression(String data) { this.data = data; }

    @Override
    public boolean interpret(String context) {
        return context.contains(data);  // Simple containment check
    }
}

// Non-terminal Expression — OR operation
public class OrExpression implements Expression {
    private Expression expr1;
    private Expression expr2;

    public OrExpression(Expression expr1, Expression expr2) {
        this.expr1 = expr1;
        this.expr2 = expr2;
    }

    @Override
    public boolean interpret(String context) {
        return expr1.interpret(context) || expr2.interpret(context);
    }
}

// Non-terminal Expression — AND operation
public class AndExpression implements Expression {
    private Expression expr1;
    private Expression expr2;

    public AndExpression(Expression expr1, Expression expr2) {
        this.expr1 = expr1;
        this.expr2 = expr2;
    }

    @Override
    public boolean interpret(String context) {
        return expr1.interpret(context) && expr2.interpret(context);
    }
}

public class Main {
    // Build expression tree: "John" OR "Jane"
    public static Expression getMaleExpression() {
        Expression john = new TerminalExpression("John");
        Expression jane = new TerminalExpression("Jane");
        return new OrExpression(john, jane);
    }

    // Build expression tree: "Julie" AND "married"
    public static Expression getMarriedWomanExpression() {
        Expression julie = new TerminalExpression("Julie");
        Expression married = new TerminalExpression("married");
        return new AndExpression(julie, married);
    }

    public static void main(String[] args) {
        Expression isMale = getMaleExpression();
        Expression isMarriedWoman = getMarriedWomanExpression();

        System.out.println("John is male? " + isMale.interpret("John"));           // true
        System.out.println("Julie is married? " + isMarriedWoman.interpret("Julie married")); // true
        System.out.println("Jack is male? " + isMale.interpret("Jack"));           // false
    }
}
```

### How It Works — Step by Step
1. `TerminalExpression` handles leaf nodes — checks if a literal exists in the context
2. `OrExpression` and `AndExpression` combine sub-expressions recursively
3. The expression tree is built by composing terminal and non-terminal expressions
4. `interpret(context)` recursively evaluates the tree against the input
5. "John OR Jane" → `OrExpression(Terminal("John"), Terminal("Jane"))`
6. Calling `interpret("John")` → `"John".contains("John") || "John".contains("Jane")` → true

### Pitfalls and Common Mistakes
- **Performance:** Recursive interpretation is slow for complex grammars — use a compiler/bytecode approach instead
- **Grammar complexity:** Only suitable for simple grammars. Complex languages need parser generators (ANTLR, JavaCC)
- **Class explosion:** Each grammar rule is a class — complex grammars create many classes

### Connection to Other Patterns
- **Composite** — the expression tree IS a composite structure
- **Flyweight** — terminal expressions with the same value can be shared
- **Visitor** can be used to traverse the expression tree for different operations
- **Iterator** can traverse the expression tree

---

## Chain of Responsibility

**GoF Category:** Behavioral

![Chain of Responsibility Diagram](27_ChainOfResponsabilityDesignPattern/ChainOfResponsabilityDesignPattern/Diagram.jpg)
![Chain of Responsibility Figure](27_ChainOfResponsabilityDesignPattern/ChainOfResponsabilityDesignPattern/figure1.jpg)

### Intent
Avoids coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. Chains the receiving objects and passes the request along the chain until an object handles it.

### When to Use
- When multiple objects may handle a request and the handler isn't known a priori
- Logging frameworks (DEBUG → INFO → WARN → ERROR)
- Servlet filters, Spring Security filter chain
- Approval workflows (employee → manager → director → VP)
- Exception handling, middleware pipelines

### Key Participants
| Class | Role |
|-------|------|
| `Handler` | Abstract handler with reference to next handler in chain |
| Concrete Handlers | Handle requests they're responsible for, pass others along |
| Client | Sends request to the first handler in the chain |

### Complete Source Code
*(Pattern 27 in the repo)*

```java
// Abstract Handler
public abstract class Logger {
    public static int INFO = 1;
    public static int DEBUG = 2;
    public static int ERROR = 3;

    protected int level;
    protected Logger nextLogger;  // Link to next handler in chain

    public void setNextLogger(Logger nextLogger) {
        this.nextLogger = nextLogger;
    }

    public void logMessage(int level, String message) {
        if (this.level <= level) {
            write(message);  // Handle if level matches
        }
        // Pass to next handler regardless (or only if not handled — varies by implementation)
        if (nextLogger != null) {
            nextLogger.logMessage(level, message);
        }
    }

    abstract protected void write(String message);
}

// Concrete Handler — Console logger
public class ConsoleLogger extends Logger {
    public ConsoleLogger(int level) { this.level = level; }

    @Override
    protected void write(String message) {
        System.out.println("Console Logger: " + message);
    }
}

// Concrete Handler — File logger
public class FileLogger extends Logger {
    public FileLogger(int level) { this.level = level; }

    @Override
    protected void write(String message) {
        System.out.println("File Logger: " + message);
    }
}

// Concrete Handler — Error logger
public class ErrorLogger extends Logger {
    public ErrorLogger(int level) { this.level = level; }

    @Override
    protected void write(String message) {
        System.out.println("Error Logger: " + message);
    }
}

public class Main {
    private static Logger getChainOfLoggers() {
        // Build the chain: Error → File → Console
        Logger errorLogger = new ErrorLogger(Logger.ERROR);
        Logger fileLogger = new FileLogger(Logger.DEBUG);
        Logger consoleLogger = new ConsoleLogger(Logger.INFO);

        errorLogger.setNextLogger(fileLogger);
        fileLogger.setNextLogger(consoleLogger);

        return errorLogger;  // Return head of chain
    }

    public static void main(String[] args) {
        Logger loggerChain = getChainOfLoggers();

        // INFO level — only ConsoleLogger handles
        loggerChain.logMessage(Logger.INFO, "Informational message");

        // DEBUG level — FileLogger and ConsoleLogger handle
        loggerChain.logMessage(Logger.DEBUG, "Debug message");

        // ERROR level — all three handle
        loggerChain.logMessage(Logger.ERROR, "Error message");
    }
}
```

### How It Works — Step by Step
1. Each logger has a `level` and a reference to the `nextLogger` in the chain
2. The chain is built: ErrorLogger → FileLogger → ConsoleLogger
3. When `logMessage(ERROR, msg)` is called on the head (ErrorLogger):
   - ErrorLogger: level(3) <= message level(3) → writes, then passes to FileLogger
   - FileLogger: level(2) <= message level(3) → writes, then passes to ConsoleLogger
   - ConsoleLogger: level(1) <= message level(3) → writes, chain ends
4. When `logMessage(INFO, msg)` is called:
   - ErrorLogger: level(3) > message level(1) → skips, passes to FileLogger
   - FileLogger: level(2) > message level(1) → skips, passes to ConsoleLogger
   - ConsoleLogger: level(1) <= message level(1) → writes, chain ends

### Pitfalls and Common Mistakes
- **Unhandled requests:** If no handler in the chain handles the request, it falls off the end silently. Add a default handler
- **Chain ordering:** The order of handlers matters — wrong order means wrong behavior
- **Performance:** Long chains add latency. Keep chains short
- **Debugging difficulty:** Hard to trace which handler processed a request

### Connection to Other Patterns
- **Composite** — the chain can be structured as a tree (each handler delegates to children)
- **Command** objects are often passed along the chain
- **Decorator** has similar linked structure but adds behavior; Chain of Responsibility finds the right handler
- Servlet `FilterChain` and Spring `HandlerInterceptor` are real-world implementations


---

# Architectural Patterns

Architectural patterns address system-level structure, defining how major components interact.

---

## MVC (Model-View-Controller)

**GoF Category:** Architectural (not strictly GoF, but foundational)

![MVC Figure 1](19_MVCDesignPattern/MVCDesignPattern/figure1.jpg)
![MVC Figure 2](19_MVCDesignPattern/MVCDesignPattern/figure2.jpg)
![MVC Figure 3](19_MVCDesignPattern/MVCDesignPattern/figure3.jpg)

### Intent
Separates an application into three interconnected components: Model (data/business logic), View (presentation/UI), and Controller (input handling/coordination). Enables independent development, testing, and modification of each concern.

### When to Use
- Web applications (Spring MVC, JSF, Struts)
- Desktop GUI applications (Swing, JavaFX)
- Mobile applications (Android Activities)
- Any application where UI changes independently of business logic
- When multiple views need to display the same data differently

### Key Participants
| Class | Role |
|-------|------|
| `Employee` | Model — holds data and business rules |
| `EmployeeDashboard` | View — renders the model for display |
| `EmployeeController` | Controller — mediates between model and view |

### Complete Source Code

```java
package com.kejeiri.java.course.model;

// MODEL — pure data, no knowledge of view or controller
public class Employee {
    private String firstName;
    private String lastName;
    private String ssNumber;
    private double salary;

    public double getSalary() { return salary; }
    public void setSalary(double salary) { this.salary = salary; }
    public String getFirstName() { return firstName; }
    public void setFirstName(String firstName) { this.firstName = firstName; }
    public String getLastName() { return lastName; }
    public void setLastName(String lastName) { this.lastName = lastName; }
    public String getSsNumber() { return ssNumber; }
    public void setSsNumber(String ssNumber) { this.ssNumber = ssNumber; }
}
```

```java
package com.kejeiri.java.course.view;
import com.kejeiri.java.course.model.Employee;

// VIEW — only responsible for displaying data
// Has no business logic, no data manipulation
public class EmployeeDashboard {
    public void printEmployeeInfo(Employee employee){
        System.out.println("FirstName: " + employee.getFirstName());
        System.out.println("LastName: " + employee.getLastName());
        System.out.println("SS number: " + employee.getSsNumber());
        System.out.println("Salary: " + employee.getSalary());
    }
}
```

```java
package com.kejeiri.java.course.controller;
import com.kejeiri.java.course.model.Employee;
import com.kejeiri.java.course.view.EmployeeDashboard;

// CONTROLLER — coordinates model and view
// Handles input, updates model, triggers view refresh
public class EmployeeController {
    private Employee employeeModel;
    private EmployeeDashboard view;

    public EmployeeController(Employee employeeModel, EmployeeDashboard view) {
        this.employeeModel = employeeModel;
        this.view = view;
    }

    // Input handling — updates the model
    public void setEmployee(String firstName, String lastName) {
        employeeModel.setFirstName(firstName);
        employeeModel.setLastName(lastName);
    }

    // Data retrieval — reads from model
    public String getEmployeeName() {
        return employeeModel.getFirstName() + " " + employeeModel.getLastName();
    }

    public void setSsNumber(String ssn) { employeeModel.setSsNumber(ssn); }
    public String getSsn() { return employeeModel.getSsNumber(); }

    // Triggers view update with current model state
    public void updateDashboardView() {
        view.printEmployeeInfo(employeeModel);
    }
}
```

```java
package com.kejeiri.java.course;
import com.kejeiri.java.course.controller.EmployeeController;
import com.kejeiri.java.course.model.Employee;
import com.kejeiri.java.course.view.EmployeeDashboard;

public class Main {
    public static void main(String[] args) {
        // Simulate fetching data (in real app: database, API, etc.)
        Employee employee = retrieveEmployeeFromServer();

        // Create view
        EmployeeDashboard view = new EmployeeDashboard();

        // Controller wires model and view together
        EmployeeController controller = new EmployeeController(employee, view);

        // Controller triggers view rendering
        controller.updateDashboardView();
    }

    public static Employee retrieveEmployeeFromServer(){
        Employee employee = new Employee();
        employee.setLastName("kejeiri");
        employee.setFirstName("mohamed");
        employee.setSsNumber("12445");
        employee.setSalary(4000.60);
        return employee;
    }
}
```

### How It Works — Step by Step
1. `Employee` (Model) is a POJO holding data — it knows nothing about how it's displayed
2. `EmployeeDashboard` (View) knows how to render an Employee but has no business logic
3. `EmployeeController` holds references to both Model and View
4. The controller provides methods to update the model (`setEmployee()`)
5. The controller provides methods to refresh the view (`updateDashboardView()`)
6. The client (`Main`) creates all three and wires them through the controller
7. Data flows: Client → Controller → Model (write) and Model → Controller → View (read/display)

### Pitfalls and Common Mistakes
- **Fat controllers:** Business logic creeps into controllers — keep them thin, push logic to model or service layer
- **View-Model coupling:** The view directly accesses the model here. In stricter MVC, the controller transforms data for the view (DTO/ViewModel)
- **Confusion with MVP/MVVM:** MVC, MVP (Model-View-Presenter), and MVVM (Model-View-ViewModel) are related but different in how they handle view updates

### Connection to Other Patterns
- **Observer** — in classic MVC, the View observes the Model for changes (not shown in this simple example)
- **Strategy** — the Controller is a strategy for the View (different controllers = different behavior)
- **Mediator** — the Controller acts as a mediator between Model and View
- **Composite** — Views are often composites (panels containing panels containing widgets)

---

# Quick Reference Summary

## Pattern Selection Guide

| Problem | Pattern | Category |
|---------|---------|----------|
| Need exactly one instance | Singleton | Creational |
| Object creation is complex/conditional | Factory | Creational |
| Object has many optional parameters | Builder | Creational |
| Need copies of existing objects | Prototype | Creational |
| Incompatible interfaces | Adapter | Structural |
| Separate abstraction from implementation | Bridge | Structural |
| Add behavior dynamically | Decorator | Structural |
| Simplify complex subsystem | Facade | Structural |
| Share objects to save memory | Flyweight | Structural |
| Control access to an object | Proxy | Structural |
| Swap algorithms at runtime | Strategy | Behavioral |
| Notify dependents of changes | Observer | Behavioral |
| Encapsulate requests as objects | Command | Behavioral |
| Define algorithm skeleton | Template Method | Behavioral |
| Traverse collection uniformly | Iterator | Behavioral |
| Object behavior depends on state | State | Behavioral |
| Centralize complex communication | Mediator | Behavioral |
| Add operations without changing classes | Visitor | Behavioral |
| Save/restore object state | Memento | Behavioral |
| Interpret a simple language | Interpreter | Behavioral |
| Pass request along a chain | Chain of Responsibility | Behavioral |
| Separate data, presentation, logic | MVC | Architectural |

## Commonly Confused Pairs

| Pattern A | Pattern B | Key Difference |
|-----------|-----------|----------------|
| Strategy | State | Client chooses strategy; state transitions internally |
| Adapter | Decorator | Adapter changes interface; Decorator adds behavior |
| Adapter | Facade | Adapter wraps one class; Facade wraps a subsystem |
| Proxy | Decorator | Proxy controls access; Decorator adds responsibility |
| Factory Method | Abstract Factory | FM creates one product; AF creates families |
| Observer | Mediator | Observer is decentralized; Mediator is centralized |
| Command | Strategy | Command = what to do + who; Strategy = how to do it |
| Template Method | Strategy | TM uses inheritance; Strategy uses composition |
| Bridge | Strategy | Bridge separates concerns; Strategy swaps algorithms |

## Patterns That Work Together

- **Command + Memento** → Undo/redo systems
- **Composite + Iterator + Visitor** → Tree traversal with operations
- **Factory + Singleton** → Single factory instance
- **Observer + Mediator** → Event-driven architectures
- **State + Flyweight** → Shared stateless state objects
- **Strategy + Factory** → Factory creates the right strategy
- **Decorator + Composite** → Recursive wrapping of tree nodes
- **Proxy + Factory** → Factory returns proxied objects (Spring AOP)

---

*Generated from Java-Design-Pattern repository analysis. All 29 patterns covered.*
