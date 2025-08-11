---
applyTo: "**"
---

# Error Handling & Recovery

## 🚨 Error Handling & Recovery

- When encountering errors, agents should provide clear diagnostic information and suggest specific remediation steps.
- Log error context for debugging and future prevention.

### AI Error Logging
When an AI error is identified (either pointed out by the user or discovered by the AI agent):

**File Location & Naming:**
- Create error log in `.github/error_logs/` directory
- Use branch-specific filename format: `{BRANCH_NAME}_AI_error_logs.md`
- Example: `PLAPP-310_AI_error_logs.md`
- Create directory and file if they don't exist

**Log Entry Format:**
```markdown
## Error Entry - {YYYY-MM-DD HH:MM:SS}

**Description:** Brief description of what went wrong
**Likely Cause:** Analysis of why the error occurred
**Mitigation Strategies:** 
- Specific steps user can take to prevent this error
- Process improvements or validation checks to implement
- Code patterns or review practices to adopt

**Context:** Additional relevant details (file paths, commands, etc.)

---
```

**When to Log:**
- User explicitly points out an AI mistake or incorrect recommendation
- AI agent discovers it made an error in previous responses
- Code implementations that fail or cause issues after AI suggestions
- Misinterpretation of requirements leading to wrong solutions
