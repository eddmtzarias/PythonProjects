# Python Projects

[![CI](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml/badge.svg)](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml)
[![Bazel Build](https://github.com/eddmtzarias/PythonProjects/actions/workflows/main.yml/badge.svg)](https://github.com/eddmtzarias/PythonProjects/actions/workflows/main.yml)
![Coverage](https://img.shields.io/badge/coverage-pending-lightgrey)
![Python](https://img.shields.io/badge/python-3.10%20%7C%203.11-blue)

Various Python projects I work on from time to time.

## Building

Projects are built using [Bazel](https://bazel.build).

- To build all projects:
  - `bazel build ...`
- To run a specific project:
  - `bazel run projects:{project} {args}`
- For example:
  - `bazel run projects:magic_eight_ball`

## Formatting

Files are formatted with [black](https://github.com/psf/black) and [isort](https://github.com/pycqa/isort).

## Development Setup

### Prerequisites

- Python 3.10 or higher
- pip

### Installation

```bash
# Clone the repository
git clone https://github.com/eddmtzarias/PythonProjects.git
cd PythonProjects

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install development dependencies
pip install -r requirements-dev.txt

# Set up pre-commit hooks
pre-commit install
```

### Running Quality Checks

```bash
# Run all pre-commit hooks
pre-commit run --all-files

# Run individual tools
black projects/              # Format code
isort projects/              # Sort imports
flake8 projects/             # Lint code
mypy projects/               # Type check

# Run tests
pytest projects/ -v

# Security checks
bandit -r projects/
pip-audit
```

### Pre-commit Hooks

This project uses pre-commit hooks to ensure code quality before commits. The hooks include:

- **black**: Code formatting
- **isort**: Import sorting
- **flake8**: Linting

To manually run hooks on all files:

```bash
pre-commit run --all-files
```
