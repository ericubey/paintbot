# CNC Pigment

## GitHub Copilot: New Conversation vs. New Agent Session

This document clarifies the difference between two distinct interaction patterns in GitHub Copilot: **new conversation** and **new agent session**.

### New Conversation (Chat Session)

A **new conversation** is a fresh chat window in Copilot Chat (such as in VS Code). It consists of your sequence of prompts and the AI's responses, including context from your current files.

#### Key Characteristics:
- **Isolated Context**: Each chat session's context is isolated—previous conversations are not referenced
- **Manual Implementation**: AI only provides suggestions; you must manually copy and apply them to your code
- **Non-Invasive**: No direct code changes unless you explicitly apply them
- **Multiple Sessions**: You can manage multiple independent chat sessions simultaneously

#### Best Used For:
- Asking programming questions
- Requesting code explanations
- Getting code snippets or advice
- Quick Q&A or learning
- Brainstorming ideas
- Organizing chats by topic or task

### New Agent Session

A **new agent session** initiates Copilot's Agent mode, transforming the AI into an autonomous coding assistant that can execute hands-on tasks.

#### Key Characteristics:
- **Full Codebase Context**: Works across multiple files with comprehensive project understanding
- **Autonomous Execution**: AI can read, edit, and run code independently
- **Iterative Problem-Solving**: Automatically responds to errors and iterates until goals are met
- **Tracked Changes**: All actions, diffs, logs, and changes can be reviewed and merged
- **Multi-Step Workflows**: Handles complex tasks requiring multiple operations

#### Best Used For:
- Multi-step tasks (refactoring, creating tests, scaffolding features)
- Cross-file edits
- Running commands and debugging
- Handling issues, feature requests, or bug fixes
- Project-wide changes
- Complex automation workflows

### Comparison Table

| Feature/Aspect | New Conversation (Chat) | New Agent Session |
|----------------|-------------------------|-------------------|
| **Context Scope** | Isolated per chat window | Full codebase, multi-file context |
| **Autonomy** | Manual—AI only suggests | Autonomous—AI executes changes |
| **Code Editing** | Manual copy/paste required | Automated, direct file editing |
| **Code Execution** | None | Can run commands, tests, build tools |
| **Use Case** | Q&A, explanations, advice | Multi-step tasks, automation |
| **Review Process** | Chat history maintained | Live logs, diffs, change tracking |
| **Control Model** | User applies all suggestions | AI manages workflow, user approves |
| **Iteration** | User-driven | AI-driven with automatic error handling |

### Best Practices

#### When to Use New Conversation:
- You need quick, targeted help or clarification
- You want to explore options without making changes
- You're learning or understanding existing code
- You prefer full manual control over all code changes

#### When to Use New Agent Session:
- You have a complex task requiring multiple file changes
- You want AI to handle the full workflow including testing
- You're comfortable with AI making direct code modifications
- You need automation for repetitive or time-consuming tasks

### Summary

**New Conversation** is ideal for simple Q&A and advice within an isolated chat environment. It's perfect when you want suggestions without automatic code changes.

**New Agent Session** empowers Copilot to act as a proactive coding assistant, handling real code changes, debugging, and automation. It's designed for deeper AI collaboration on your codebase.

Both modes are valuable tools, and the choice depends on your specific needs: use conversations for guidance and agent sessions for execution.
