# Python Calculator Project

A simple yet robust calculator implementation in Python, featuring basic arithmetic operations with proper error handling and testing.

## Features

- Basic arithmetic operations:
  - Addition
  - Subtraction
  - Multiplication
  - Division (with zero division protection)
- Type hints for better code clarity
- Comprehensive test coverage
- CI/CD pipeline using GitHub Actions

## Project Structure

```
.
├── swe2/
│   ├── __init__.py
│   ├── calculator.py    # Core calculator implementation
│   └── main.py         # Example usage and demo
├── tests/
│   └── test_calculator.py  # Test suite
├── .github/
│   └── workflows/
│       └── ci.yml      # CI configuration
└── pyproject.toml      # Project dependencies and metadata
```

## Installation

This project uses Poetry for dependency management. To get started:

1. Make sure you have Python 3.12+ installed
2. Install Poetry if you haven't already:
   ```bash
   curl -sSL https://install.python-poetry.org | python3 -
   ```
3. Install dependencies:
   ```bash
   poetry install
   ```

## Usage

The calculator can be used either as a module or through the demo script:

```python
from swe2.calculator import Calculator

# Create calculator instance
calc = Calculator()

# Perform operations
result1 = calc.add(5, 3)      # Returns 8
result2 = calc.subtract(10, 4) # Returns 6
result3 = calc.multiply(6, 7)  # Returns 42
result4 = calc.divide(15, 3)   # Returns 5.0
```

To run the demo script:

```bash
poetry run python swe2/main.py
```

## Testing

The project includes a comprehensive test suite. To run the tests:

```bash
poetry run pytest
```

## CI/CD

The project uses GitHub Actions for continuous integration, automatically running tests on:

- Push to main branch
- Pull requests to main branch

## Error Handling

The calculator includes proper error handling, particularly for division by zero operations:

```python
try:
    calc.divide(10, 0)
except ValueError as e:
    print(f"Error: {e}")  # Prints: Error: Cannot divide by zero
```

## Author

Mostafa Kassem <elkasem2012@gmail.com>
