# GitHub Copilot Prompts & Instructions

A collection of structured prompts and instructions for maximizing productivity with GitHub Copilot and AI coding assistants. These resources help create consistent, high-quality code with proper testing, documentation, and development workflows.

## What's Included

### Core Instructions

- **[Base Instructions](/.github/copilot-instructions-base.md)** - Language-agnostic development patterns and best practices
- **[Java/Spring Boot Instructions](/.github/copilot-instructions-java.md)** - Java-specific conventions and patterns
- **[Main Instructions](/.github/copilot-instructions.md)** - Project-specific workflow integration

### Structured Prompts

Located in `.github/prompts/`:

| Prompt | Purpose | Usage |
|--------|---------|-------|
| **[code-assessment](/.github/prompts/code-assessment.prompt.md)** | Analyze project structure and conventions | `/code-assessment` |
| **[create-goal-plan](/.github/prompts/create-goal-plan.prompt.md)** | Create structured implementation plans | `/create-goal-plan` |
| **[implement-plan](/.github/prompts/implement-plan.prompt.md)** | Execute plans with atomic commits | `/implement-plan <name>` |
| **[list-plans](/.github/prompts/list-plans.prompt.md)** | View all plans and their progress | `/list-plans [status]` |

## Key Features

### Development Workflow

1. **Structured Planning** - Break down complex features into manageable tasks
2. **Atomic Commits** - One logical change per commit with clear messages
3. **Testing Strategy** - Always include unit tests for new features
4. **Agent Delegation** - Parallelize work with GitHub Copilot Agent

### Code Quality Standards

- **Immutability preferred** - Use const/final/readonly where possible
- **Dependency injection** over global state
- **Clear error handling** - Handle expected errors gracefully
- **No hardcoded values** - Use configuration and environment variables
- **Security first** - Never commit secrets, use secure defaults

### Testing Requirements

- Use project's standard testing framework
- Test with actual dependencies when appropriate
- Place tests in matching package/directory structure
- Aim for meaningful coverage of logic paths

## 📋 Usage Examples

### Quick Development Workflow

```bash
# 1. Understand the project
/code-assessment

# 2. Plan a new feature
/create-goal-plan

# 3. Implement step by step
/implement-plan user-authentication

# 4. Check progress
/list-plans active
```

### Commit Message Format

```text
Short summary (50 chars or less)

Detailed explanation if needed. Wrap at 72 characters.
Explain the what and why, not the how.

Signed-off-by: Your Name <your.email@example.com>
```

## 🛠️ Integration

### GitHub Copilot Chat

Place the instruction files in your repository's `.github/` directory. GitHub Copilot will automatically reference them when providing suggestions and code reviews.

### Custom Prompts

The structured prompts in `.github/prompts/` can be used with:

- GitHub Copilot Chat
- VS Code extensions
- Command-line AI tools
- Custom development workflows

## Best Practices

### Before Making Changes

1. Understand the project structure and conventions
2. Read relevant existing code
3. Check for similar implementations
4. Identify affected test files

### Development Cycle

1. **Plan** - Break down work into small, testable increments
2. **Implement** - Write minimal code to achieve the goal
3. **Test** - Create/update tests to verify behavior
4. **Validate** - Run build, tests, linters
5. **Commit** - Atomic commit with clear message
6. **Repeat** - Next increment

## 🎨 Customization

### For Your Project

1. Copy the base instructions to your repository's `.github/` directory
2. Modify `copilot-instructions.md` to reference your project specifics
3. Create language-specific instruction files if needed
4. Adapt the structured prompts for your workflow

### Language Support

The base instructions are language-agnostic. Create specific instruction files for:

- `copilot-instructions-python.md`
- `copilot-instructions-typescript.md`
- `copilot-instructions-dotnet.md`
- etc.

## Contributing

Feel free to:

- Suggest improvements to existing prompts
- Add new structured prompts for common scenarios
- Share language-specific instruction patterns
- Report issues or inconsistencies

## License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.

## Related Resources

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [AI Coding Best Practices](https://docs.github.com/en/copilot/using-github-copilot/best-practices-for-using-github-copilot)
- [Spring Boot Development Guidelines](https://spring.io/guides)

## Reference

- [Awesome Copilot](https://github.com/github/awesome-copilot)

---

Happy coding with AI assistance! 🤖✨
