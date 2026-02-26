# The Pragmatic Programmer Core Principles

## Chapter 1 - A Pragmatic Philosophy

### 1. The Cat Ate My Source Code (Take Responsibility)
- Take responsibility for your career
- Provide options, don't make excuses

### 2. Software Entropy (Technical Debt)
- Don't live with broken windows (bad code)
- Fix problems when you see them, don't wait for them to worsen

### 3. Stone Soup and Boiled Frogs
- Be a catalyst for change
- Remember the big picture, don't get overwhelmed by details

### 4. Good-Enough Software
- Involve users in quality trade-offs
- Know when to stop; perfect is the enemy of done

### 5. Your Knowledge Portfolio
- Continuous learning
- Think critically about what you read and hear

### 6. Communicate!
- Share ideas with your audience
- Organize content from the audience's perspective

## Chapter 2 - A Pragmatic Approach

### 7. The Evils of Duplication (DRY)
- Every piece of knowledge must have a single, unambiguous, authoritative representation
- Not just code, but also comments, documentation, data, APIs

### 8. Orthogonality
- Eliminate effects between unrelated things
- Increase productivity and reduce risk
- Avoid global data, avoid similar functions

### 9. Reversibility
- Keep decisions reversible
- Avoid casting decisions in stone

### 10. Tracer Bullets
- Find the target through end-to-end early implementation
- Tracer bullets vs prototypes: Tracer bullets are kept, prototypes are discarded

### 11. Prototypes and Post-it Notes
- Learn with prototypes, then discard
- Architecture prototypes focus on system components and interactions

### 12. Domain Languages
- Program in your application's domain language
- Consider creating mini-languages or DSLs

### 13. Estimating
- Estimate to avoid surprises
- Model-based estimating

## Chapter 3 - The Basic Tools

### 14. The Power of Plain Text
- Plain text never goes out of style

### 15. Shell Games
- Use the power of command shells

### 16. Power Editing
- Master one editor

### 17. Source Code Control
- Always use version control

### 18. Debugging
- Debugging is problem solving, not blame
- Don't panic, let the data tell you
- Find root causes, don't treat symptoms

### 19. Text Manipulation
- Learn a text manipulation language

### 20. Code Generators
- Don't write code that writes code; write code that generates code

## Chapter 4 - Pragmatic Paranoia

### 21. Design by Contract
- Preconditions, postconditions, class invariants
- Crash early

### 22. Dead Programs Tell No Lies
- Detect problems early, crash early
- Don't catch exceptions and do nothing

### 23. Assertive Programming
- If it can't happen, use assertions to ensure it won't
- Assertions for things that shouldn't happen, not error handling

### 24. When to Use Exceptions
- Use exceptions for exceptional problems
- Exceptions should not be used for normal program flow

### 25. Balancing Resources
- Finish what you start: Functions/objects that allocate resources should release them
- Balance resource acquisition and release

## Chapter 5 - Bend or Break

### 26. Decoupling and the Law of Demeter
- Law of Demeter for functions: Only talk to immediate friends
- Avoid train wrecks: a.b.c.d.doSomething()

### 27. Metaprogramming
- Configure, don't integrate
- Put abstractions in code, details in metadata

### 28. Temporal Decoupling
- Use services for architectural analysis
- Concurrency and temporal decoupling

### 29. It's Just a View
- Separate views from models
- Publish/Subscribe pattern

### 30. Blackboards
- Use blackboards to coordinate workflows

## Chapter 6 - While You Are Coding

### 31. Programming by Coincidence
- Don't program by coincidence; understand the code you write
- Rely on reliable things

### 32. Algorithm Speed
- Estimate algorithmic complexity: O(n), O(log n), etc.

### 33. Refactoring
- Refactor early, refactor often
- Refactor when adding functionality
- Refactor when fixing bugs
- Refactor during code review

### 34. Code That's Easy to Test
- Design for testing from the start
- Test-driven development

### 35. Evil Wizards (Code Generation)
- Don't trust wizard-generated code you don't understand

## Chapter 7 - Before the Project

### 36. The Requirements Pit
- Dig for requirements, don't assume
- Work with users to understand their thinking

### 37. Solving Impossible Puzzles
- When facing constraints, identify the real constraints
- Sometimes the answer is "don't do that"

### 38. Not Until You're Ready
- Listen to your intuition
- Sometimes you need to say "no"

### 39. The Specification Trap
- Specifications don't give you experience
- Over-specification becomes a burden

### 40. Circles and Arrows (UML and Diagrams)
- Don't worship diagrams
- Diagrams are tools, not the goal

## Chapter 8 - Pragmatic Projects

### 41. Pragmatic Teams
- Don't tolerate broken windows
- Be a catalyst for change

### 42. Ubiquitous Automation
- Don't use manual procedures for what machines can do
- Automate builds, tests, deployments

### 43. Ruthless Testing
- Test early, test often, test automatically
- Test coverage is your friend
- Use saboteurs to test environment recovery

### 44. It's All Writing (Naming)
- Write code in English
- Keep it clear and precise

### 45. Pragmatic Starter Kit
- Version control, regression testing, full automation

### 46. Sign Your Work (Assertions and Exceptions)
- Don't assume; assert or throw exceptions

### 47. Different Environments, Different Languages
- Use the right language for the job
- Polyglot programming

### 48. Pragmatic Estimation Rules
- The rule of estimation completeness
- The rule of estimation uncertainty

### 49. Pragmatic Paranoia
- Contracts, assertions, and exceptions

### 50. Pragmatic Projects
- Small steps forward, continuous feedback

## Practical Tips Summary

- DRY (Don't Repeat Yourself)
- Orthogonality
- ETC (Easier to Change) - This is the most important principle
- Tracer bullets
- Prototypes and post-it notes
- Domain languages
