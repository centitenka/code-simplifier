---
name: code-simplifier
description: |
  Code review and refactoring based on principles from "Clean Code",
  "Clean Architecture", and "The Pragmatic Programmer". Trigger when users request:
  1. "review/refactor this code" mentioning code quality principles
  2. "refactor based on Clean Code/Clean Architecture"
  3. "review code quality/architecture design"
  4. "identify code smells"
  5. "refactor this code" with focus on design quality

  Supports multiple languages, with module-level or project-level review options.
---

# Code Review and Refactoring

Perform code review and refactoring based on principles from "Clean Code", "Clean Architecture", and "The Pragmatic Programmer".

## Reference Documents

- [clean-code-principles.md](references/clean-code-principles.md) - Naming, functions, classes, comments, and code-level principles
- [clean-architecture-principles.md](references/clean-architecture-principles.md) - Architecture design, dependencies, and layering principles
- [pragmatic-programmer-principles.md](references/pragmatic-programmer-principles.md) - DRY, orthogonality, design by contract principles

## Workflow

### Phase 1: Exploration and Understanding

1. **Determine Review Scope**
   - Ask user about desired granularity (module/package level vs project level)
   - Identify target programming language and tech stack
   - Understand project's business domain and core functionality

2. **Code Exploration**
   - Read core source files to understand existing code structure
   - Identify project's architectural patterns (if any)
   - Understand module/package dependencies
   - Identify key business logic and data flow

### Phase 2: Principle Application and Issue Identification

Check code against the following principles, reading reference documents as needed:

#### Clean Code Checklist

**Naming**
- [ ] Are names intention-revealing?
- [ ] Are there misleading names?
- [ ] Are class names nouns/noun phrases?
- [ ] Are method names verbs/verb phrases?
- [ ] Are searchable names used (avoid single letters/magic numbers)?

**Functions**
- [ ] Are functions small (<20 lines)?
- [ ] Do functions do one thing?
- [ ] Are there <= 2 parameters?
- [ ] Are there side effects?
- [ ] Is Command Query Separation followed?
- [ ] Are exceptions used instead of return codes?

**Comments**
- [ ] Do comments explain "why" not "what"?
- [ ] Are there redundant/misleading comments?
- [ ] Can comments be replaced with better naming?

**Classes**
- [ ] Do classes have single responsibility?
- [ ] Is class cohesion good?
- [ ] Are classes loosely coupled?

#### Clean Architecture Checklist

**Dependency Rule**
- [ ] Do dependencies point inward toward the core?
- [ ] Do high-level modules depend on abstractions rather than low-level modules?

**SOLID Principles**
- [ ] SRP: Does each class/module have only one reason to change?
- [ ] OCP: Is it open for extension, closed for modification?
- [ ] LSP: Can subtypes replace base types?
- [ ] ISP: Are interfaces small and focused?
- [ ] DIP: Does it depend on abstractions, not concrete implementations?

**Boundaries & Layers**
- [ ] Are there clear layers (Entities, Use Cases, Adapters)?
- [ ] Are external framework dependencies isolated?
- [ ] Is business logic decoupled from UI/database/external services?

#### The Pragmatic Programmer Checklist

**DRY (Don't Repeat Yourself)**
- [ ] Is knowledge duplicated (code, config, documentation)?
- [ ] Can similar code be eliminated through abstraction?

**Orthogonality**
- [ ] Does modifying one module affect others?
- [ ] Is there global state?

**ETC (Easier to Change)**
- [ ] Does the current design make future changes easier?
- [ ] Are decisions reversible?

**Law of Demeter**
- [ ] Are there train wrecks (a.b.c.doSomething())?
- [ ] Do functions only talk to immediate friends?

### Phase 3: Refactoring Plan

1. **Priority Ranking**
   - High priority: Issues affecting correctness, security, performance
   - Medium priority: Issues affecting maintainability, readability
   - Low priority: Style consistency issues

2. **Dependency Analysis**
   - Determine refactoring dependency order
   - Identify which refactorings must be done sequentially
   - Identify which refactorings can be done in parallel

### Phase 4: Execute Refactoring

Follow these principles when refactoring:

1. **Small Steps**
   - Make one small change at a time
   - Ensure code remains functional after each change

2. **Preserve Behavior**
   - Refactoring should not change external behavior
   - Keep interface contracts unchanged

3. **Common Refactoring Techniques**
   - Rename: Improve naming
   - Extract Function: Break down large functions
   - Inline: Eliminate unnecessary indirection
   - Move: Improve code organization
   - Extract Class: Separate responsibilities
   - Introduce Parameter Object: Reduce parameter count
   - Replace Conditional with Polymorphism: Eliminate complex conditionals

### Phase 5: Verify Correctness

**Must ensure code correctness after refactoring**:

1. **Static Analysis**
   - Ensure code compiles/parses correctly
   - Check type consistency
   - Check for syntax errors

2. **Logical Equivalence Check**
   - Verify logical equivalence before and after refactoring
   - Check boundary condition handling consistency
   - Verify error handling paths are preserved

3. **Test Coverage**
   - If existing tests exist, ensure they still pass
   - If tests are missing, suggest adding tests for refactored parts

### Phase 6: Documentation and Summary

1. **Change Summary**
   - List all modifications
   - Explain which principle each modification follows
   - Explain the motivation for changes

2. **Follow-up Recommendations**
   - Suggest future refactoring directions
   - Suggest tests that need to be added
   - Suggest architecture improvements

## Language-Specific Guidelines

### Python
- Follow PEP 8 style guide
- Use type annotations for clarity
- Leverage context managers (with statements)
- Watch for mutable default argument issues

### Java/TypeScript
- Handle null properly (Optional/Nullable)
- Use interfaces and abstract classes appropriately
- Use generics correctly
- Use Stream/Collection APIs appropriately

### JavaScript
- Avoid var, use let/const
- Choose between arrow functions and regular functions
- Use Promise/async-await correctly
- Avoid implicit type coercion

### Go
- Error handling patterns (return error)
- Implicit interface implementation
- Avoid overusing interfaces (YAGNI)
- Proper goroutine and channel usage

### Rust
- Proper ownership and lifetime usage
- Result/Option handling
- Avoid overusing macros
- Proper trait usage

### C/C++
- Resource management (RAII)
- Safe pointer and reference usage
- Avoid memory leaks
- Const correctness

## Common Refactoring Scenarios

### Scenario 1: Large Functions/God Classes
**Problem**: Functions over 50 lines, or classes with too many responsibilities
**Refactoring**: Extract functions, extract classes, apply SRP

### Scenario 2: Deep Nesting
**Problem**: Multiple nested if/for/while loops
**Refactoring**: Early returns, guard clauses, extract functions, polymorphism

### Scenario 3: Duplicate Code
**Problem**: Same or similar code appearing multiple times
**Refactoring**: Extract functions, introduce template method, use strategy pattern

### Scenario 4: Tight Coupling
**Problem**: Modules depend on each other, hard to modify independently
**Refactoring**: Dependency injection, interface segregation, event-driven

### Scenario 5: Anemic Domain Model
**Problem**: Business logic scattered in service layer, entities only have getters/setters
**Refactoring**: Move business logic into domain objects, introduce value objects

### Scenario 6: Framework Dependency
**Problem**: Business logic mixed with framework code
**Refactoring**: Introduce adapter layer, repository pattern, dependency inversion

## Quality Gates

Before submitting refactoring results, ensure:

1. [ ] All modifications have clear principle-based rationale
2. [ ] Logical equivalence is maintained before and after refactoring (behavior unchanged)
3. [ ] Code readability is improved
4. [ ] No new code smells are introduced
5. [ ] Dependencies are improved (if architecture refactoring)
