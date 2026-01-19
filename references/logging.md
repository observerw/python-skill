# Logging Guidelines

## Library

- MUST use [loguru](https://loguru.readthedocs.io/en/stable/) for all logging requirements.
- Do NOT use the standard `logging` module unless strictly required by external dependencies that cannot be overridden.

## Structure

- Consult with the user to design a reasonable logging structure (e.g., file rotation, log levels, output formats) before implementation.
- Ensure logging provides sufficient context for debugging without cluttering standard output.

## Exception Handling

- Prohibited Patterns: Do NOT use broad `except Exception` blocks that swallow errors. Always re-raise exceptions or log them fully with stack traces in specific handlers.
- Global Catch: Ensure all unhandled exceptions are captured at the application entry point (e.g., using `@logger.catch` on `main`) to prevent silent crashes.

## Best Practices

- Structured Logging: Prefer `.bind(user_id=...)` over string formatting (f-strings).
- Async & Performance: MUST set `enqueue=True`.
- Security: Strict audit required. NEVER log sensitive information like passwords, API keys, or tokens.
- Environment Strategy:
  - Development: Use colorful console output for readability.
  - Production: Use JSON format and write to files for machine parsing and archiving.
