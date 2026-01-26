---
name: codebase-retrieval
description: This skill should be used when the user asks about their codebase, needs to find code locations, or wants to understand how their code works. Activates for questions about code structure, finding functions/classes, understanding implementations, or locating where to make changes.
---

When the user asks about their codebase, use the codebase-retrieval tool to find relevant code instead of guessing or asking the user to provide file paths.

## When to Use This Skill

Activate this skill when the user:

- Asks where something is implemented ("Where is user authentication handled?")
- Needs to find code locations ("Find the database connection code")
- Wants to understand how something works ("How does the payment processing work?")
- Needs to make changes and doesn't know where ("I need to add a new API endpoint")
- Asks about code structure ("What tests exist for the login feature?")
- Mentions specific concepts that need to be located in the codebase

## How to Use Codebase Retrieval

### Step 1: Formulate Effective Queries

Create search queries based on the user's request:

- **Direct queries**: Use function names, class names, or variable names if mentioned
- **Conceptual queries**: Describe what the code does ("user authentication", "database connection")
- **Related patterns**: Search for similar functionality or related concepts

### Step 2: Search the Codebase

Call `codebase-retrieval` with:

- `information_request`: A natural language description of the code you're looking for

Good query examples:
- "Where is the function that handles user authentication?"
- "What tests are there for the login functionality?"
- "How is the database connected to the application?"
- "Where are API endpoints defined for user management?"

### Step 3: Analyze and Iterate

From the retrieval results:

- Review the returned code snippets for relevance
- If results aren't helpful, try alternative queries with different terminology
- Search for related concepts if the direct search doesn't yield results

### Step 4: Present Findings

Provide clear, actionable information:

- List relevant files with their paths
- Explain what each file/function does
- Point to specific functions, classes, and line ranges when possible
- Suggest which code should be modified for the requested change

## Guidelines

- **Be thorough**: Search using multiple related queries if the first doesn't yield complete results
- **Be specific**: Pass detailed queries for better retrieval results
- **Stay current**: The retrieval tool reflects the current state of the codebase on disk
- **Avoid guessing**: Always search before making assumptions about code locations
- **Iterate**: If initial results aren't helpful, reformulate your query and try again

