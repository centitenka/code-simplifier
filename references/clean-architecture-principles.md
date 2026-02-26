# Clean Architecture Core Principles

## Chapter 1 - What is Design and Architecture

- No difference between design and architecture
- Goal: Minimize human cost, maximize productivity

## Chapter 2 - The Two Values of Software

- Behavior value: Implementing functional requirements
- Architecture value: The "soft" in software, ease of change
- Prioritize keeping architecture healthy

## Part 2 - Structured Programming

- Sequence, selection, iteration are the foundation of all programs

## Part 3 - Object-Oriented Programming

- OO essence is dependency management
- Polymorphism: The mechanism to cross architectural boundaries

## Part 4 - Functional Programming

- Immutability reduces concurrency issues

## Part 5 - Design Principles (SOLID)

### SRP - Single Responsibility Principle
- A module should have only one reason to change
- Method-level SRP: Functions do one thing
- Class-level SRP: Only one responsibility

### OCP - Open/Closed Principle
- Open for extension, closed for modification
- Achieved through abstraction and interfaces

### LSP - Liskov Substitution Principle
- Subtypes must be substitutable for their base types
- Inheritance must respect behavioral contracts

### ISP - Interface Segregation Principle
- Clients should not depend on interfaces they don't use
- Split fat interfaces into smaller ones

### DIP - Dependency Inversion Principle
- High-level modules should not depend on low-level modules; both should depend on abstractions
- Abstractions should not depend on details; details should depend on abstractions
- Dependencies should point toward more stable abstractions

## Part 6 - Component Principles

### REP - Reuse/Release Equivalence Principle
- The granule of reuse is the granule of release

### CCP - Common Closure Principle
- Classes that change together belong together

### CRP - Common Reuse Principle
- Classes that are used together belong together
- Don't depend on what you don't need

### Component Coupling Principles
- Acyclic Dependencies Principle (ADP): No cycles in component dependency graph
- Stable Dependencies Principle (SDP): Depend in the direction of stability
- Stable Abstractions Principle (SAP): Components should be as abstract as they are stable

## Part 7 - Architecture

### What is Architecture
- Architecture is the shape of the system, how components are partitioned
- Goal: Minimize human resources needed to build and maintain the system

### Independence
- Use case independence
- Operational independence (deployment, development, maintenance)
- Technical independence

### Boundaries
- Boundaries are the most important part of software architecture
- Boundaries separate components at different abstraction levels
- Boundary crossing is the most expensive operation in architecture

### Anatomy of Boundaries
- Monolith: Source-level boundaries
- Deployment components: Binary-level boundaries
- Services: Process-level boundaries

### Policy and Level
- Levels are defined by distance from inputs and outputs
- Source code dependencies must point toward higher-level policies
- Stable architectures are easier to change

### Business Rules
- Entities: Critical business logic and data
- Use cases: Application-specific logic

### Screaming Architecture
- Architecture should scream the purpose of the system
- Frameworks are tools, not the architecture itself

### Clean Architecture
- Dependency Rule: Dependencies point inward toward the core
- Layers: Entities → Use Cases → Interface Adapters → Frameworks & Drivers
- Crossing boundaries: Use Dependency Inversion Principle

### Presenters and Humble Objects
- Separate hard-to-test parts from easy-to-test parts
- UI, database, external service interfaces should be humble objects

### Partial Boundaries
- Partially implemented architectural boundaries for future separation

### Layers and Boundaries
- Systems may need layering along multiple dimensions

### The Main Component
- The most detail-heavy component, initializes dependencies, loads configuration

### Services: Great and Small
- Services are not architectural boundaries, only process boundaries

### Test Boundaries
- Tests are part of the system, follow same design principles

### Clean Embedded Architecture
- Hardware details should be separated from business logic
