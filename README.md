# Python Projects

[![CI](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml/badge.svg)](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Imports: isort](https://img.shields.io/badge/%20imports-isort-%231674b1?style=flat&labelColor=ef8336)](https://pycqa.github.io/isort/)
[![Checked with mypy](https://img.shields.io/badge/mypy-checked-blue)](http://mypy-lang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Various Python projects I work on from time to time.

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/eddmtzarias/PythonProjects.git
cd PythonProjects

# Install development dependencies
pip install -r requirements-dev.txt

# Install pre-commit hooks
pre-commit install
```

## 🏗️ Building

Projects are built using [Bazel](https://bazel.build).

```bash
# Build all projects
bazel build ...

# Run a specific project
bazel run projects:{project} {args}

# Example
bazel run projects:magic_eight_ball
```

## 🧪 Development

### Code Quality Checks

```bash
# Format code with black
black projects/

# Sort imports with isort
isort projects/

# Lint with flake8
flake8 projects/

# Type check with mypy
mypy projects/
```

### Testing

```bash
# Run tests
pytest

# Run tests with coverage
pytest --cov=projects --cov-report=html
```

### Security Checks

```bash
# Security scan with bandit
bandit -r projects/

# Check for vulnerable dependencies
pip-audit

# Detect secrets
detect-secrets scan
```

### Pre-commit Hooks

```bash
# Run all hooks on all files
pre-commit run --all-files
```

## 📚 Documentation

```bash
# Serve docs locally
mkdocs serve

# Build docs
mkdocs build
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENCE) file for details.
