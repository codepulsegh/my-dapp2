# Quality Gates

| Field | Value |
|-------|-------|
| Type | `repo-quality-gates` |
| ID | `3633f08d` |
| Category | quality |
| Tags | ci, cd, testing, linting, quality |
| Description | CI/CD, testing, linting |

## Configuration

| Setting | Value |
|---------|-------|
| Ci Provider | github-actions |
| Test Framework | vitest |
| Linter | biome |
| Formatter | biome |
| Typecheck | Enabled |
| Pre Commit Hooks | Enabled |
| Coverage Threshold | 80 |
| Security Scanning | Enabled |
| Dependency Audit | Enabled |

## Scripts

| Name | Command |
|------|---------|
| `lint` | `biome lint .` |
| `lint:fix` | `biome lint --write .` |
| `format` | `biome format --write .` |
| `format:check` | `biome format .` |
| `test` | `vitest run` |
| `test:coverage` | `vitest run --coverage` |
| `typecheck` | `tsc --noEmit` |
| `prepare` | `husky` |

## Documentation

### Code Quality Guidelines

# Code Quality Guidelines

This document describes the code quality tools and standards used in this project.

## Overview

| Tool | Purpose | Command |
|------|---------|---------|
| biome | Linting | `pnpm lint` |
| biome | Formatting | `pnpm format` |
| vitest | Testing | `pnpm test` |
| TypeScript | Type Checking | `pnpm typecheck` |

## Linting

We use **biome** for code linting.

```bash
# Check for lint errors
pnpm lint

# Auto-fix lint errors
pnpm lint:fix
```

## Formatting

We use **biome** for code formatting.

```bash
# Format all files
pnpm format

# Check formatting without modifying
pnpm format:check
```

## Testing

We use **vitest** for testing.

```bash
# Run all tests
pnpm test

# Run tests with coverage
pnpm test:coverage
```

### Coverage Requirements

- Minimum coverage threshold: **80%**
- Coverage report is generated in the `coverage/` directory


## Type Checking

TypeScript is used for type safety.

```bash
pnpm typecheck
```



## Pre-commit Hooks

This project uses Husky and lint-staged to run quality checks before commits.

The following checks run automatically:
- Lint staged files
- Format staged files
- Type check the entire project

To bypass hooks in emergencies (not recommended):
```bash
git commit --no-verify -m "your message"
```


## CI/CD


GitHub Actions runs the following checks on every PR:

1. **Lint** - Ensures code follows style guidelines
2. **Format** - Verifies code formatting
3. **Test** - Runs the test suite with coverage
4. **Typecheck** - Validates TypeScript types
5. **Security Scan** - Checks for vulnerabilities
6. **Dependency Audit** - Audits npm dependencies


## Best Practices

1. Run `pnpm lint:fix && pnpm format` before committing
2. Write tests for new features
3. Maintain 80%+ test coverage
4. Keep dependencies up to date
5. Address lint warnings, don't suppress them


## File Structure

This component would generate the following files:

- `.github/workflows/ci.yml`
- `biome.json`
- `vitest.config.ts`
- `tsconfig.json`
- `.husky/pre-commit`
- `.lintstagedrc`
- `.editorconfig`

## Integration Points

**Depends on:**
- Stylus-rust-contract (`f15e8607`)

**Provides to:**
- Auditware-analyzing (`270ee821`)

