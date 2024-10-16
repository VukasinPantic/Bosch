# Development GUIDELINE


## Code Formatting

- Adhere to PEP8 standards for code style
- Line length <= 79 characters, for better readability
- Indentation: 4 spaces
- Imports at the top of the file; on separate lines if not a part of the same library. Grouping standard libraries, third-party libraries, and local imports separately. Avoid wildcard `imports (“ from module import \* ”)`; There should be no unused imports
- Use line breaks for long statements and function calls for better readability.
- Blank Lines: two blank lines surround top-level function and class definitions; single blank line surrounds class methods; + blank lines in functions, sparingly, to indicate logical sections
- Surround operators with single space on each side
- If operators with different priorities are used, consider adding whitespace (single space) around the operators with the lowest priority
- Avoid trailing whitespace anywhere !
- No whitespace around ‘=‘ sign when used for keyword arguments

## Naming Conventions

- **snake_case** for variable and function names
- **PascalCase** for class names
- Constants all **UPPERCASE** with words separated by underscores
- Prefix unused variables or arguments with an underscore or use underscore only.

## Function and Method Design

- Small and focused functions, adhering to Single Responsibility Principle
- Usage of type hints when applicable
- Docstrings for functions (and classes) when deemed necessary, explaining parameters, return values, and behavior
- Default function arguments should never be mutable objects like lists or dictionaries

## Error Handling

- Catch and handle exceptions by using try/except blocks, wherever necessary
- Avoid catching broad exceptions like Exception unless necessary
- **Custom exceptions** for domain-specific error handling

## Version Control

- Commit code frequently with concise, meaningful commit messages

**EXAMPLE: ? *decide***

Fix: correct index out of range error

Feat: add user login functionality

- Use a **feature branch workflow** for all new work, merge into the main branch only after code review
- Never commit secrets (e.g., API keys, passwords) or large binary files to the repository

## Documentation

- Write **README** files for new projects or features, explaining usage, setup, and any special considerations.
- Ensure code is self-explanatory; avoid unnecessary comments, but use comments to clarify complex logic or when using a workaround for specific issue
- Inline Comments should be used sparingly, when really needed, and separated by at least two spaces from the statement on the left

## Testing

- Write **unit tests** for all functions and methods, aiming for high code coverage
- Unittest/pytest framework for automated testing
- Mock external dependencies and APIs during testing to avoid side effects and isolate the function of interest
- Ensure tests are successful before pushing any code
- tests are structured in a “ tests/ “ directory

## Dependency Management

- Pin versions in requirements.txt to avoid unexpected changes from dependency updates
- Regularly update requirements.txt with exact library versions

## Logging and Monitoring

- Logging: use logging module to report errors instead of print() - for production code
- Log at appropriate levels (DEBUG, INFO, WARNING, ERROR, CRITICAL)

Code example (python):

`import logging`

`logging.basicConfig(level=logging.INFO)`

`logging.error(“An error occurred!”)`



**Python environment** 

- Pip/brew package manager
- Virtualenv package for virtual environments
- Pylint for live linting (+ pre-commit hook)

**SECURITY CHECKER ?**

*Bandit library ?*  :smile: