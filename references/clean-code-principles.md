# Clean Code Core Principles

## Chapter 1 - Clean Code

- Code is communication (to the next reader)
- Boy Scout Rule: Leave the campground cleaner than you found it

## Chapter 2 - Meaningful Names

- Intention-revealing names: Names should express intent
- Avoid disinformation: Avoid type information, reserved words
- Make meaningful distinctions: Avoid meaningless number sequences
- Use searchable names: Avoid single letters and magic numbers
- Class names: Nouns or noun phrases
- Method names: Verbs or verb phrases
- One word per concept: Consistent terminology

## Chapter 3 - Functions

- Small: Functions should do one thing
- Single Responsibility Principle (SRP)
- One abstraction level per function
- Use descriptive names
- Function arguments: Ideal is 0, then 1, then 2, avoid 3+
- No side effects: Functions should only do what they promise
- Command Query Separation
- Use exceptions rather than return codes
- Don't Repeat Yourself (DRY)

## Chapter 4 - Comments

- Comments cannot clean up bad code
- Express intent in code, not comments
- Good comments: Legal info, intent explanation, TODOs, warnings
- Bad comments: Mumbling, redundant comments, misleading comments, mandative comments, journal comments

## Chapter 5 - Formatting

- Vertical formatting: Related concepts close, unrelated separated
- Vertical distance: Variable declarations close to usage
- Horizontal formatting: Proper indentation, reasonable line length

## Chapter 6 - Objects and Data Structures

- Data abstraction: Hide implementation details
- Law of Demeter: Modules should not know internals of objects they manipulate
- Data Transfer Objects (DTO)

## Chapter 7 - Error Handling

- Use exceptions rather than return codes
- Write Try-Catch-Finally first
- Use unchecked exceptions
- Provide context with exceptions
- Define exception classes based on caller's needs

## Chapter 8 - Boundaries

- Maintain clear boundaries when using third-party code
- Learning tests: Understand third-party library behavior
- Use Adapter pattern to encapsulate boundaries

## Chapter 9 - Unit Tests

- TDD Three Laws
- Keep tests clean
- One assertion per concept
- FIRST principles: Fast, Independent, Repeatable, Self-Validating, Timely

## Chapter 10 - Classes

- Class organization: Constants, variables, public functions, private utilities
- Classes should be small: Single Responsibility Principle
- Cohesion: Each variable should be used by each method
- Isolate modification: Open/Closed Principle (OCP), Dependency Inversion Principle (DIP)

## Chapter 17 - Smells and Heuristics

- Comments: Inappropriate information, obsolete comments, redundant comments
- Functions: Too many arguments, output arguments, flag arguments
- General issues: Deep nesting, tight coupling, feature envy, selector parameters, obscure intent
