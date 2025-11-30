# Getting Started

This guide will help you set up your development environment for contributing to PythonProjects.

## Prerequisites

- Python 3.10 or later
- pip (Python package manager)
- Git

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/eddmtzarias/PythonProjects.git
cd PythonProjects
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install Development Dependencies

```bash
pip install -r requirements-dev.txt
```

### 4. Install Pre-commit Hooks

```bash
pre-commit install
```

## Running Quality Checks

### Code Formatting

```bash
# Format with black
black projects/

# Sort imports with isort
isort projects/
```

### Linting

```bash
# Run flake8
flake8 projects/

# Run mypy type checking
mypy projects/
```

### Testing

```bash
# Run tests with pytest
pytest

# Run tests with coverage
pytest --cov=projects --cov-report=html
```

### Security Checks

```bash
# Run bandit security linter
bandit -r projects/

# Check for vulnerable dependencies
pip-audit

# Detect secrets
detect-secrets scan
```

## Building with Bazel

This project also supports building with Bazel:

```bash
# Build all projects
bazel build ...

# Run a specific project
bazel run projects:magic_eight_ball
```

## Documentation

```bash
# Serve docs locally
mkdocs serve

# Build docs
mkdocs build
```
