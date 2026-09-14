---
description: 'TypeScript formatting, comments, and API documentation standards'
applyTo: '**/*.{ts,astro}'
---

# TypeScript Coding Standards

## Comments

- Comment intent, constraints, tradeoffs, or non-obvious decisions. Do not restate what the next line of code does.
- Prefer clear names and small functions over comments that explain mechanics.
- Treat an outdated or misleading comment as a bug. Update or remove it in the same change that changes the related behavior.
- Keep temporary investigation notes and commented-out code out of committed source.

## API Documentation

- Use TSDoc/JSDoc (`/** ... */`) for API contracts and regular comments (`//`) only for local implementation decisions.
- Every exported function in `db/` and `src/lib/` must document its purpose, every parameter with `@param`, and its return value with `@returns`.
- Keep documentation specific enough to explain observable behavior, including ordering, nullability, determinism, side effects, or thrown errors when relevant.
- Give exported functions explicit parameter and return types. ESLint enforces this at module boundaries.
- Document reusable Astro component `Props` interfaces as described in [`astro.instructions.md`](astro.instructions.md).

## Formatting

- Use four spaces for indentation; do not use tabs.
- Use single quotes for TypeScript strings and terminate statements with semicolons.
- Add trailing commas to multiline arrays, objects, parameter lists, and imports.
- Keep one declaration per line and use braces for multiline control flow.
- Use `import type` when an import is used only as a type. ESLint enforces consistent type-only imports.
- Let ESLint own enforceable conventions. Do not add formatter-only churn to unrelated code, and do not disable a lint rule without documenting the reason.
