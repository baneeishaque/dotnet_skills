```markdown
# dotnet_skills Development Patterns

> Auto-generated skill from repository analysis

## Overview
The `dotnet_skills` repository provides a collection of C# code samples and utilities for developing .NET skills, focusing on best practices in code organization, naming conventions, and modularity. This skill teaches you how to structure C# projects with clear naming, consistent import/export patterns, and maintainable test files, even without a specific framework.

## Coding Conventions

### File Naming
- **Convention:** Use PascalCase for all file names.
- **Example:**  
  `SkillManager.cs`, `UserProfile.cs`

### Import Style
- **Convention:** Use relative imports to reference other files within the project.
- **Example:**
  ```csharp
  using MyProject.Utilities;
  ```

### Export Style
- **Convention:** Use named exports for classes and methods.
- **Example:**
  ```csharp
  public class SkillManager
  {
      public void AddSkill(string skillName) { /* ... */ }
  }
  ```

### Commit Patterns
- **Convention:** Commit messages are freeform, with no strict prefixing, and average around 66 characters.

## Workflows

### Adding a New Skill Module
**Trigger:** When you need to add a new skill or feature to the codebase.  
**Command:** `/add-skill-module`

1. Create a new C# file using PascalCase (e.g., `NewSkill.cs`).
2. Define your class with named exports.
   ```csharp
   public class NewSkill
   {
       public void Execute() { /* ... */ }
   }
   ```
3. Use relative imports in other files to reference your new module.
4. Write corresponding test files using the `*.test.*` pattern.

### Refactoring Imports
**Trigger:** When reorganizing code or moving files.  
**Command:** `/refactor-imports`

1. Update all `using` statements to use the correct relative paths.
2. Ensure all references are consistent with the new file structure.

### Writing Tests
**Trigger:** When adding new features or fixing bugs.  
**Command:** `/write-tests`

1. Create a test file matching the pattern `*.test.*` (e.g., `SkillManager.test.cs`).
2. Write test cases for each public method in your module.
3. Use the available (unknown) test framework conventions.

## Testing Patterns

- **File Pattern:** Test files follow the `*.test.*` naming convention.
  - **Example:** `SkillManager.test.cs`
- **Framework:** The specific testing framework is not detected, so follow general C# testing patterns.
- **Test Structure:** Write tests for each public method, ensuring coverage and maintainability.

## Commands
| Command             | Purpose                                      |
|---------------------|----------------------------------------------|
| /add-skill-module   | Scaffold a new skill module                  |
| /refactor-imports   | Update import statements after code changes  |
| /write-tests        | Create or update test files for your modules |
```
