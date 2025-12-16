# Python Pack

**Version: 0.2.1**

Modern Python development setup with ruff (linting + formatting), mypy (type checking), pytest, and pre-commit hooks.

## Contents

### python-gitignore
Standard ignore patterns for Python projects. Covers:
- Bytecode (`__pycache__/`, `*.pyc`)
- Virtual environments (`.venv/`, `venv/`)
- Distribution files (`dist/`, `*.egg-info/`)
- Test/coverage outputs (`.pytest_cache/`, `.coverage`)
- Type checker caches (`.mypy_cache/`, `.ruff_cache/`)

### python-workspace
Complete Python project starter with:
- **Python 3.11+** - Modern Python features
- **ruff** - Fast linter and formatter (replaces black, isort, flake8)
- **mypy** - Strict type checking
- **pytest** - Testing with coverage support
- **pre-commit** - Git hooks for automated checks
- **Makefile** - Common development commands

## Usage

1. Install the pack via ProjectHub
2. Create a new project and select `python-workspace`
3. Set up your environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   make dev
   ```

## Available Commands

| Command | Description |
|---------|-------------|
| `make dev` | Install package with dev dependencies |
| `make lint` | Run ruff linter |
| `make lint-fix` | Auto-fix lint issues |
| `make format` | Format code with ruff |
| `make typecheck` | Run mypy type checking |
| `make test` | Run pytest |
| `make test-cov` | Run tests with HTML coverage report |
| `make clean` | Remove build artifacts |
| `make hooks` | Install git hooks |
| `make hooks-run` | Run all hooks manually |

## Git Hooks

Pre-commit hooks are automatically installed when you run `make dev`. The hooks check for:
- Sensitive data (email, username, API keys, passwords)
- Sensitive files (.env, .pem, .key, etc.)
- Ruff linting and formatting
- Mypy type checking

## Compatibility

- ProjectHub >= 1.0
- Python >= 3.11
