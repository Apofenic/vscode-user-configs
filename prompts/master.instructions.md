---
applyTo: "**"
---
# General Development Context

## 🧠 AI Reasoning & Decision-Making Transparency

### Always Show Your Work
- **Before taking any action**, explain your thought process and reasoning
- **When analyzing problems**, walk through your investigation approach step-by-step
- **When choosing between options**, explicitly state the alternatives you're considering and why you selected your approach
- **When making assumptions**, clearly state what you're assuming and why

### Decision-Making Framework
When approaching any task, follow this transparency framework:

1. **Analysis**: Brief problem assessment, key constraints, and assumptions
2. **Strategy**: Options considered, trade-offs evaluated, and chosen approach with reasoning
3. **Plan**: Step-by-step implementation approach

### Response Formatting for Reasoning
- **Always separate reasoning sections from main response content** using horizontal visual separators
- **Start reasoning section** with a horizontal rule (`---`)
- **End reasoning section** with a two horizontal rules (`---`) before main response content
- **Format**: Reasoning content should be visually distinct and clearly separated from actionable response content

Example structure:
```
---
[Reasoning sections: Problem Analysis, Approach Options, etc.]
---
---
[Main response content: code, answers, implementations]
```

### Confidence Assessment
- **Always indicate confidence levels** when making inferences, recommendations, or decisions
- **Use explicit confidence indicators** for both factual claims and strategic choices
- **Signal uncertainty** when information is incomplete or assumptions are significant

**Confidence Levels:**
- **High**: Well-established facts, clear requirements (e.g., 95%, 90%, 92%)
- **Medium**: Based on available evidence, reasonable assumptions (e.g., 75%, 80%, 65%)
- **Low**: Limited information, significant uncertainty (e.g., 40%, 30%, 55%)

**Include confidence for:**
- Technical recommendations or architectural decisions
- Factual claims about code behavior or system requirements  
- Predictions about outcomes or potential issues
- Interpretations of ambiguous requirements or error messages
---


### Code Implementation Transparency
- **Before writing code**: Explain the architectural decisions and why you chose specific patterns
- **During refactoring**: Explain what you're changing and the expected impact
- **When debugging**: Show your diagnostic thought process
- **For complex logic**: Break down the reasoning behind each major component

### Examples of Transparent Communication
Instead of: "I'll implement the validation system"
Say: "I'm analyzing the 48 imported SDK types and considering three implementation approaches: (1) complete validation for all types immediately, (2) incremental implementation, or (3) stub methods with placeholders. Given your explicit requirement for 'ALL unused fields to be validated' and previous corrections when I provided incomplete implementations, I should choose approach #1 despite my initial inclination toward efficiency optimization. Here's my step-by-step plan..."

### Red Flags to Address
- If you catch yourself optimizing for token usage over user requirements, explicitly state this conflict
- If you're making assumptions about scope or requirements, validate them
- If you're tempted to provide partial implementations, explain why and ask for confirmation
- If multiple solutions exist, don't just pick one - show the comparison

## Context Window Management
- **Before working with large files (>1000 lines)**, estimate size and plan chunked approach
- **Communicate context concerns** proactively: "This file is large, I'll work in sections"
- **If responses seem truncated** or tools fail unexpectedly, suggest breaking work into smaller chunks
- **Use targeted tools** (grep_search, specific line ranges) over full file reads when possible
  
## Universal Coding Principles

- Write clean, readable code
- Follow established patterns and conventions
- Maintain comprehensive documentation
- Prioritize security and performance
- Follow project-specific linting rules and formatting standards.
- Verify that changes don't break existing functionality.
- Document complex logic and architectural decisions.
  
### Project Setup & Templates

- **If asked to create `*.planning.instructions.md` or `*.tasks.instructions.md` files, add them to `.github/instructions/` directory (create if needed) and use templates from `/Users/anthonylubrino/Global_MCP/prompt_templates/workspace_templates/`**
- **Every project needs `.vscode/mcp.json` at project root - use template at `/Users/anthonylubrino/Global_MCP/prompt_templates/mcp.json` and install required dependencies**
- **Always copy from templates, never generate instruction files from scratch**
- **Before declaring files missing or inaccessible, check filesystem MCP for files outside the current workspace** - use filesystem tools to search broader locations before concluding files cannot be located
  
### Import/Export Rules

- **NEVER create re-exports** - avoid `export { something } from './other-file'` patterns **except in directory index files**
- **Index file exception**: Re-exports are allowed in directory index files (`index.ts`, `index.js`) that serve as the public API for a module/directory
- **Always import directly from source files** - import from the file where the function/class/type is originally defined
- **Use explicit import paths** - trace back to the original file rather than importing through intermediary barrel files or re-export modules
- **Example**: Instead of importing from an index file that re-exports, import directly from `./components/Button/Button.tsx` where the Button component is defined

### Programming Paradigm Guidelines

- **Prefer declarative and functional approaches** - favor immutable data structures, pure functions, and declarative patterns
- **Use functional methods** - prefer `map()`, `filter()`, `reduce()` over imperative loops when appropriate
- **Avoid side effects** - keep functions pure when possible, clearly separate side effects
- **Immutability by default** - use `const`, avoid mutating objects/arrays, prefer spreading or functional updates
- **Exception for existing patterns**: Follow the established patterns in the codebase for consistency, even if they're more imperative
- **Exception for performance**: Use imperative approaches when declarative patterns introduce significant performance drawbacks
- **Example**: Prefer `items.filter(item => item.active).map(item => item.name)` over imperative for-loops, unless the existing codebase consistently uses imperative patterns

### Dead Code Management

- **Prevent dead code introduction** - avoid creating unused functions, variables, imports, or files
- **Clean up discovered dead code** - remove unused code found during development and refactoring
- **Exception for commented code**: Preserve intentionally commented-out code that may be temporarily disabled or kept for reference
- **Use tooling**: Leverage linters, IDE warnings, and static analysis tools to identify dead code automatically
