# Python Projects

[![CI](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml/badge.svg)](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml)
[![Bazel Build](https://github.com/eddmtzarias/PythonProjects/actions/workflows/main.yml/badge.svg)](https://github.com/eddmtzarias/PythonProjects/actions/workflows/main.yml)
[![codecov](https://codecov.io/gh/eddmtzarias/PythonProjects/branch/main/graph/badge.svg)](https://codecov.io/gh/eddmtzarias/PythonProjects)
[![PyPI version](https://badge.fury.io/py/pythonprojects.svg)](https://badge.fury.io/py/pythonprojects)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)

Various Python projects I work on from time to time.

## Building

Projects are built using [Bazel](https://bazel.build).

- To build all projects:
  - `bazel build ...`
- To run a specific project:
  - `bazel run projects:{project} {args}`
- For example:
  - `bazel run projects:magic_eight_ball`

## Development Setup

### Prerequisites

- Python 3.10 or higher
- pip

### Setting up the development environment

```bash
# Clone the repository
git clone https://github.com/eddmtzarias/PythonProjects.git
cd PythonProjects

# Create and activate a virtual environment (recommended)
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install development dependencies
pip install -r requirements-dev.txt

# Set up pre-commit hooks
pre-commit install
```

### Running code quality checks

```bash
# Run all pre-commit hooks
pre-commit run --all-files

# Run individual tools
black --check projects/
isort --check-only projects/
flake8 projects/
mypy projects/
```

### Running tests

```bash
# Run tests with coverage
pytest tests/ --cov=projects --cov-report=term-missing

# Run tests without coverage
pytest tests/
```

### Running security scans

```bash
# Run Bandit security linter
bandit -r projects/ -ll

# Run pip-audit for dependency vulnerabilities
pip-audit
```

## Formatting

Files are formatted with [black](https://github.com/psf/black) and imports are sorted with [isort](https://github.com/pycqa/isort).

```bash
# Format all files
black projects/
isort projects/
```
