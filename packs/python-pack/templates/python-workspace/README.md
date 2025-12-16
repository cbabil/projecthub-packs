# Python Workspace

A Python project template with modern tooling.

## Setup

Create a virtual environment and install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
make dev
```

## Development

| Command | Description |
|---------|-------------|
| `make lint` | Run ruff linter |
| `make lint-fix` | Fix lint issues |
| `make format` | Format code with ruff |
| `make typecheck` | Run mypy type checking |
| `make test` | Run tests with pytest |
| `make test-cov` | Run tests with coverage report |
| `make clean` | Remove build artifacts |

## Project Structure

```
.
├── src/           # Source code
├── tests/         # Test files
├── pyproject.toml # Project configuration
├── Makefile       # Development commands
└── README.md
```
