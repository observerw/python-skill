---
name: python
description: Comprehensive guide for the entire Python programming process. This skill MUST be consulted before writing any code in a Python project to ensure adherence to toolchains, standards, and best practices.
---

# Python Programming Guide

## Toolchain

ALWAYS use `--help` if more information about the cli tool is needed.

- Type Checking: `ty check <FILE_PATH> --output-format concise`
- Lint: `ruff check --fix --unsafe-fixes <FILE_PATH>`
  - Unsafe fixes are allowed, but you MUST review changes before committing
- Format: `ruff format <FILE_PATH>`
- Run tests: `uv run pytest`
- Sync deps: `uv sync --upgrade`
- NEVER use `python`; use `uv run` instead

## Async Programming

- Always use [`anyio`](https://anyio.readthedocs.io/en/stable/)

## Mandatory Reading (Context-Specific)

You MUST read the following documents when performing related tasks:

- **Exception Design**: Read `references/exceptions.md` when designing, refactoring, or debugging error handling and custom exceptions.
- **Logging Guidelines**: Read `references/logging.md` before adding or modifying logging calls, or when configuring loggers.
- **Linting and Code Quality**: Read `references/linting.md` before performing code reviews, fixing linting errors, or starting any refactoring task.
- **Type Hints**: Read `references/type-hints-cheat-sheet.md` when adding type annotations to complex data structures, generics, or protocol definitions.
