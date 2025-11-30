# Python Projects

[![CI](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml/badge.svg)](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml)
[![CodeFactor](https://www.codefactor.io/repository/github/eddmtzarias/pythonprojects/badge)](https://www.codefactor.io/repository/github/eddmtzarias/pythonprojects)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Imports: isort](https://img.shields.io/badge/imports-isort-blue.svg)](https://pycqa.github.io/isort/)
[![Type checked: mypy](https://img.shields.io/badge/type%20checked-mypy-blue.svg)](https://mypy-lang.org/)

Various Python projects I work on from time to time.

## Building

Projects are built using [Bazel](https://bazel.build).

- To build all projects:
  - `bazel build ...`
- To run a specific project:
  - `bazel run projects:{project} {args}`
- For example:
  - `bazel run projects:magic_eight_ball`

## Developer Setup

### Prerequisites

- Python 3.10 or higher
- pip (Python package manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/eddmtzarias/PythonProjects.git
   cd PythonProjects
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install development dependencies:
   ```bash
   pip install -r requirements-dev.txt
   ```

4. Install pre-commit hooks:
   ```bash
   pre-commit install
   ```

### Running Quality Checks

Run all pre-commit hooks:
```bash
pre-commit run --all-files
```

Run individual checks:
```bash
# Formatting
black .
isort .

# Linting
flake8 .

# Type checking
mypy projects/

# Tests with coverage
pytest
coverage run -m pytest
coverage report

# Security scanning
bandit -r projects/ -ll
```

## Formatting

Files are formatted with [Black](https://github.com/psf/black) and imports are sorted with [isort](https://pycqa.github.io/isort/).
