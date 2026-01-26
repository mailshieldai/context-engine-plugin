# Augment Context Engine Plugin for Claude Code

Bring full codebase context into your AI workflows. The Augment Context Engine MCP delivers deep semantic understanding across large, long-lived codebases, including architecture, dependencies, and history. Use it to move beyond file-level prompts, plan changes with confidence, and automate complex tasks safely. Make system-level context a native input to your agents so AI can operate reliably on real-world production software.

## What's Included

This plugin provides:

- **MCP Server** - Connects Claude Code to Augment's context engine service
- **Skills** - Auto-triggers codebase retrieval when you ask about your code
- **Agents** - A dedicated `context-expert` agent for focused code localization

## Installation

Add the marketplace and install the plugin:

```bash
claude plugin marketplace add augmentcode/augment-plugin
claude plugin install augment-context-engine@augment-marketplace
```

## Available Tools

### codebase-retrieval

Searches your codebase using natural language queries and returns relevant code snippets.

```
Input: "Where is user authentication handled?"
Output: Relevant code snippets with file paths and line numbers
```

Key features:
- Uses proprietary retrieval/embedding models for high-quality recall
- Maintains a real-time index of your codebase
- Retrieves across different programming languages
- Reflects the current state of files on disk

## Usage Examples

The plugin works automatically when you ask about your codebase:

- "Where is the function that handles user authentication?"
- "What tests are there for the login functionality?"
- "How is the database connected to the application?"
- "Where should I add a new API endpoint?"

Or spawn the context-expert agent when you want focused code localization:

```
spawn context-expert to find all the payment processing code
```

## When to Use

The codebase-retrieval tool is ideal for:

- **Finding code locations** - Locate functions, classes, or implementations
- **Understanding structure** - Learn how different parts of the codebase connect
- **Planning changes** - Identify all files that need modification
- **Finding tests** - Locate existing tests for specific functionality
- **Code exploration** - Discover how features are implemented

## Best Practices

- **Be specific**: Detailed queries yield better results
- **Use natural language**: Describe what you're looking for conceptually
- **Iterate**: If initial results aren't helpful, try alternative terminology
- **Combine with other tools**: Use results to guide further exploration with file viewing

