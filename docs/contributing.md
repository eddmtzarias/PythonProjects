# Contributing

Thank you for your interest in contributing to PythonProjects!

## Development Workflow

1. **Fork the repository** on GitHub
2. **Clone your fork** locally
3. **Create a branch** for your changes
4. **Make your changes** and ensure they pass all checks
5. **Submit a pull request**

## Code Quality Requirements

Before submitting a PR, ensure your code passes all quality checks:

### Formatting

```bash
# Format code with black
black projects/

# Sort imports with isort
isort projects/
```

### Linting

```bash
# Check code style
flake8 projects/

# Type checking
mypy projects/
```

### Testing

```bash
# Run tests
pytest

# Run tests with coverage
pytest --cov=projects
```

### Security

```bash
# Security scan
bandit -r projects/

# Dependency audit
pip-audit
```

## Pre-commit Hooks

We use pre-commit hooks to automatically run checks before each commit:

```bash
# Install hooks
pre-commit install

# Run hooks manually on all files
pre-commit run --all-files
```

## Pull Request Guidelines

- **Keep changes focused**: One feature or fix per PR
- **Write clear commit messages**: Describe what and why
- **Update documentation**: If your change affects usage
- **Add tests**: For new functionality
- **Follow the code style**: Use black and isort

## Reporting Issues

If you find a bug or have a feature request:

1. Check if an issue already exists
2. Open a new issue with a clear description
3. Include steps to reproduce (for bugs)

## Questions?

Feel free to open an issue for questions or discussions.
