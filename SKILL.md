---
name: python
description: Comprehensive guide for the entire Python programming process. This skill MUST be consulted before writing any code in a Python project to ensure adherence to toolchains, standards, and best practices.
---

# Python Programming Guide

## Toolchain

- Type Checking: `ty check <FILE_PATH> --output-format concise`
- Lint: `ruff check --fix --unsafe-fixes <FILE_PATH>`
  - Unsafe fixes are allowed, but you must review changes before committing
- Format: `ruff format <FILE_PATH>`
- Run tests: `uv run pytest`
- Sync latest deps: `uv sync --upgrade`
- NEVER use `python`; use `uv run` instead

## Async Programming

- Always use [`anyio`](https://anyio.readthedocs.io/en/stable/)

## References

- [Linting and Code Quality](references/linting.md): MUST be read first when aiming to improve code quality.
