.PHONY: install dev lint format typecheck test clean hooks

install:
	pip install -e .

dev:
	pip install -e ".[dev]"
	pre-commit install

lint:
	ruff check .

lint-fix:
	ruff check . --fix

format:
	ruff format .

format-check:
	ruff format . --check

typecheck:
	mypy src

test:
	pytest

test-cov:
	pytest --cov=src --cov-report=html

clean:
	rm -rf .ruff_cache .mypy_cache .pytest_cache .coverage htmlcov
	find . -type d -name __pycache__ -exec rm -rf {} +
	find . -type f -name "*.pyc" -delete

hooks:
	pre-commit install

hooks-run:
	pre-commit run --all-files
