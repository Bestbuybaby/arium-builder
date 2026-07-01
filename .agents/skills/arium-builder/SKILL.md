```markdown
# arium-builder Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `arium-builder` repository, a TypeScript project built with the Next.js framework. You'll learn about file naming, import/export styles, commit conventions, and how to write and locate tests in this codebase.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `userProfile.ts`, `dataFetcher.tsx`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In userProfile.ts
    export function getUserProfile(id: string) { ... }
    ```

    ```typescript
    // Importing
    import { getUserProfile } from './userProfile';
    ```

### Commit Patterns
- Commit messages are **freeform** (no strict prefixes or types).
- Average commit message length is about 63 characters.
  - Example:
    ```
    Fix bug in user profile rendering when data is missing
    ```

## Workflows

_No explicit workflows were detected in this repository._

## Testing Patterns

- **Test File Pattern:** Test files use the `*.test.*` naming convention.
  - Example: `userProfile.test.ts`
- **Testing Framework:** Not explicitly detected, but test files are present.
- **How to Write Tests:** Place test files alongside or near the modules they test, using the `*.test.ts` or `*.test.tsx` pattern.

  ```typescript
  // userProfile.test.ts
  import { getUserProfile } from './userProfile';

  test('returns correct user profile', () => {
    const profile = getUserProfile('123');
    expect(profile.id).toBe('123');
  });
  ```

## Commands

| Command | Purpose |
|---------|---------|
| /test   | Run all test files matching `*.test.*` |
| /lint   | Lint the codebase according to project conventions |
| /build  | Build the Next.js project |
```