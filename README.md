# Python Projects

[![CI](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml/badge.svg)](https://github.com/eddmtzarias/PythonProjects/actions/workflows/ci.yml)
[![codecov](https://codecov.io/gh/eddmtzarias/PythonProjects/branch/main/graph/badge.svg)](https://codecov.io/gh/eddmtzarias/PythonProjects)

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

Files are formatted with [yapf](https://github.com/google/yapf).

## Development Setup

### Prerequisites

- Python 3.10 or 3.11
- pip

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

4. Set up pre-commit hooks:
   ```bash
   pre-commit install
   ```

### Running Quality Checks

Run pre-commit hooks on all files:
```bash
pre-commit run --all-files
```

Run individual checks:
```bash
# Formatting
black projects/
isort projects/

# Linting
flake8 projects/

# Type checking
mypy projects/

# Tests
pytest projects/ -v

# Security scanning
bandit -r projects/
pip-audit
```
