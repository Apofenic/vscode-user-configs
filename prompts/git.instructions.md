---
applyTo: "**"
---

# Git & Version Control Best Practices

## 🔄 Version Control Best Practices

### Commit Message Guidelines

Follow conventional commit format: `type(scope): description`

**Commit Types:**

- **feat**: New feature or functionality
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code formatting, whitespace, or style changes
- **refactor**: Code restructuring without changing functionality
- **test**: Adding or updating tests
- **chore**: Maintenance tasks, dependency updates

**Writing Guidelines:**

- Keep the first line under 72 characters
- Use imperative mood (e.g., "add", "fix", "update" not "added", "fixed", "updated")
- Include scope when relevant to specify the area of change
- Use lowercase for type and scope
- Don't end with a period
- Keep the total commit message length under 250 characters

**El Toro Project Standards:**

- Include ticket numbers when applicable: `feat(PLAPP-265): add DDC database validation`
- For breaking changes, add `!` after the type/scope: `feat!: change API structure`

**Examples:**

- `feat(auth): add two-factor authentication`
- `fix(validation): resolve null pointer in user input`
- `docs(api): update authentication endpoints`
- `refactor(utils): extract common validation logic`
- `test(auth): add integration tests for login flow`
- `chore(deps): update lodash to v4.17.21`

### Git Workflow

- Check git status before making significant changes
- Suggest appropriate commit messages for changes made using the guidelines above
- Be aware of branch context and avoid conflicts
- Respect `.gitignore` patterns when creating new files
