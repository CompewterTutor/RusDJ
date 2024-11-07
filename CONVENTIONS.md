# Engineering Conventions

## Conventions
> When writing code, follow these conventions

- Write simple, verbose code over terse, compact, dense code
- If a function does not have a corresponding test, mention it
- When building tests, don't mock anything
- Unit tests should be placed in the same module they are testing at the bottom, for more complex modules, create a tests/ subdirectory within the module folder
- Place integration tests in the tests/ directory at the root level. These tests focus on the interaction between different parts of the application
- UI tests using slint should be placed under ui/tests


## Project Structure
