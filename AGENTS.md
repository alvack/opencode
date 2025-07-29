## Build/Lint/Test Commands

- `bun install` - Install all dependencies
- `bun run dev` - Run CLI in development mode
- `bun run typecheck` - Type check all packages
- `bun run packages/opencode/test/bun.test.ts` - Run a single test file
- `cd packages/sdk && ./scripts/test path/to/test.file.ts` - Run a single SDK test
- `cd packages/sdk && ./scripts/lint` - Lint SDK code
- `cd packages/sdk && ./scripts/format` - Format SDK code
- `cd packages/sdk && ./scripts/build` - Build SDK

## Code Style Guidelines

### Imports
- Use relative imports within the same package
- Avoid package imports like `@opencode-ai/sdk` in source code
- Prefer single word variable/function names
- Group imports logically (external, internal, types)

### Formatting
- Use Prettier with semi=false, printWidth=120 (root) or printWidth=110 (SDK)
- Use single quotes for strings
- Trailing commas required
- No unused imports (enforced by eslint)

### Types
- Strict TypeScript with all strict flags enabled
- Use Zod for schema validation
- No implicit any, strict null checks
- Exact optional property types

### Naming Conventions
- Prefer single word variable/function names
- Use camelCase for variables and functions
- Use PascalCase for classes and types
- Use UPPER_CASE for constants

### Error Handling
- Avoid try/catch where possible - let exceptions bubble up
- Avoid else statements where possible
- Do not create useless helper functions - inline unless reusable

### General
- Prefer Bun APIs
- Use descriptive variable/function names when single word isn't clear
- Follow existing code patterns in the codebase
- Write clean, robust, high-quality code with clear logic