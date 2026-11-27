# Python-capstone-project
# Simple Calculator

A beginner-friendly command-line calculator written in Python. It asks for two numbers and an operation, then prints the result.

## Features

- Addition, subtraction, multiplication and division
- Works with whole numbers and decimals
- Handles division by zero without crashing
- Handles invalid input (such as letters instead of numbers)

## Requirements

- Python 3.x (no external libraries needed)

## How to Run

1. Save the code as `capstone.py`.
2. Open a terminal in the same folder.
3. Run:

```bash
python calculator.py
```

## Usage

```
===== Simple Calculator =====
1. Addition
2. Subtraction
3. Multiplication
4. Division
Enter first number: 10
Enter second number: 4
Enter your choice (1-4): 4
Result: 2.5
```

| Choice | Operation      |
|--------|----------------|
| 1      | Addition       |
| 2      | Subtraction    |
| 3      | Multiplication |
| 4      | Division       |

## How the Code Works

### Functions

| Function         | Purpose                                                              |
|------------------|----------------------------------------------------------------------|
| `add(a, b)`      | Returns `a + b`                                                      |
| `subtract(a, b)` | Returns `a - b`                                                      |
| `multiply(a, b)` | Returns `a * b`                                                      |
| `divide(a, b)`   | Returns `a / b`, or a message if `b` is 0 (uses `try/except`)        |

### Program Flow

1. Prints the menu of operations.
2. Reads two numbers with `input()` and converts them using `float()`.
3. Reads the user's choice (`"1"` to `"4"`) as a string.
4. Uses `if / elif / else` to call the matching function and print the result.
5. If the choice is not 1 to 4, prints `Invalid choice!`.

### Error Handling

| Situation                  | What happens                                    |
|----------------------------|-------------------------------------------------|
| Dividing by zero           | `divide()` catches `ZeroDivisionError` and returns `Cannot divide by zero!` |
| Typing text, not a number  | `float()` raises `ValueError`, and the program prints `Please enter valid numbers!` |
| Choice outside 1 to 4      | Prints `Invalid choice!`                        |

## Concepts Demonstrated

- Defining and calling functions
- Taking user input and type conversion
- Conditional statements (`if`, `elif`, `else`)
- Exception handling (`try`, `except`)

## Limitations and Future Improvements

- Runs only one calculation per execution. A `while` loop could allow repeated calculations.
- `divide()` returns a string on error, which mixes types. Raising an error or returning `None` would be cleaner.
- Could add more operations, such as modulus, power and square root.

## License

Free to use for learning and practice.
