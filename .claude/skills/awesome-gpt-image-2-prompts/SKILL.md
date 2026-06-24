```markdown
# awesome-gpt-image-2-prompts Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `awesome-gpt-image-2-prompts` TypeScript repository. It covers file organization, code style, commit message standards, and testing practices. By following these guidelines, contributors can ensure consistency and maintainability across the codebase.

## Coding Conventions

### File Naming
- **Style:** Snake case
- **Example:**  
  ```plaintext
  image_prompt_utils.ts
  prompt_generator.test.ts
  ```

### Import Style
- **Relative imports are used throughout the codebase.**
- **Example:**
  ```typescript
  import { generatePrompt } from './prompt_utils';
  ```

### Export Style
- **Named exports are preferred.**
- **Example:**
  ```typescript
  // In prompt_utils.ts
  export function generatePrompt(input: string): string { ... }
  ```

### Commit Messages
- **Conventional commit format**
- **Prefix:** `fix`
- **Example:**
  ```
  fix: correct prompt parsing for edge cases
  ```

## Workflows

### Fixing a Bug
**Trigger:** When a bug is identified in the codebase  
**Command:** `/fix-bug`

1. Create a new branch for your fix.
2. Make code changes following the coding conventions.
3. Write or update tests in a `*.test.ts` file.
4. Commit using the `fix:` prefix (e.g., `fix: handle empty prompt input`).
5. Push your branch and open a pull request.

### Adding a New Utility Function
**Trigger:** When you need to add reusable logic  
**Command:** `/add-utility`

1. Create a new file using snake_case (e.g., `new_utility.ts`).
2. Implement the function and use named exports.
3. Add or update tests in a corresponding `*.test.ts` file.
4. Import the utility using a relative path where needed.
5. Commit your changes with a descriptive message.

## Testing Patterns

- **Test files use the pattern:** `*.test.ts`
- **Testing framework:** Not explicitly detected; follow standard TypeScript test practices.
- **Example:**
  ```typescript
  // prompt_generator.test.ts
  import { generatePrompt } from './prompt_generator';

  describe('generatePrompt', () => {
    it('returns a valid prompt string', () => {
      expect(generatePrompt('cat')).toContain('cat');
    });
  });
  ```
- Place test files alongside their corresponding modules or in a dedicated test directory.

## Commands
| Command      | Purpose                                 |
|--------------|-----------------------------------------|
| /fix-bug     | Start the bug fixing workflow           |
| /add-utility | Add a new utility function to the codebase |
```
