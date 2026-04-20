# Development Setup

Additional dependencies for development and testing.

## Installation

```bash
pip install -r requirements-dev.txt
```

## Development Tools

- **pytest**: Testing framework
- **black**: Code formatting
- **flake8**: Linting
- **pylint**: Code analysis
- **mypy**: Type checking

## Commands

### Run Tests
```bash
pytest tests/
```

### Format Code
```bash
black .
```

### Lint Code
```bash
flake8 .
```

### Type Check
```bash
mypy .
```

### All Checks
```bash
black .
flake8 .
mypy .
pytest tests/
```

## Project Standards

- Python 3.8+
- PEP 8 style guide
- Docstrings for all functions
- Type hints for parameters and returns

## Contributing

1. Create feature branch
2. Make changes
3. Run format and lint checks
4. Submit pull request
