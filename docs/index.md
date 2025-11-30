# Python Projects

Welcome to the Python Projects documentation!

## Overview

This repository contains various Python projects developed for learning and experimentation purposes.

## Projects

The `projects/` directory contains multiple Python scripts including:

- **Calculator** - Mathematical operations on two numbers
- **FizzBuzz** - Classic FizzBuzz implementation
- **Fibonacci** - Fibonacci sequence generator
- **Blackjack** - Card game simulation
- **Tic Tac Toe** - Classic game implementation
- **Caesar Cipher** - Encryption/decryption tool
- **Vigenere Cipher** - Advanced encryption tool
- **Dice Roller** - Random dice simulation
- **Magic Eight Ball** - Fortune telling simulation
- And many more!

## Getting Started

### Prerequisites

- Python 3.10 or higher
- pip (Python package manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/eddmtzarias/PythonProjects.git
   cd PythonProjects
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install development dependencies:
   ```bash
   pip install -r requirements-dev.txt
   ```

### Running Projects

Projects can be run individually:
```bash
python projects/fizz_buzz.py
python projects/calculator.py
```

Or using Bazel:
```bash
bazel run projects:fizz_buzz
```

## Development

See the main [README](https://github.com/eddmtzarias/PythonProjects/blob/main/README.md) for development instructions.
