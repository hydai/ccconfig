# Claude Configuration Repository

A centralized repository for managing Claude AI configurations including agents, commands, and hooks.

## Overview

This repository serves as a collection of reusable Claude AI configurations to enhance developer productivity and enable consistent AI-powered workflows. It follows a spec-driven development approach with clear structure and documentation.

## Repository Structure

```
ccconfig/
├── agents/          # AI agent configurations
├── commands/        # Custom command definitions
├── hooks/           # Event-driven hooks
└── docs/            # Documentation and specifications
```

## Features

### Agents
Pre-configured AI agents for specific tasks:
- **code-reviewer**: Performs thorough code reviews focusing on quality, maintainability, and best practices
- **requirements-analyst**: Transforms vague ideas into clear User Stories with Gherkin acceptance criteria
- **system-architect**: Creates technical designs from requirements
- **agile-task-decomposer**: Breaks features into INVEST-compliant tasks
- **task-executor**: Executes tasks from structured task lists

### Commands
Custom commands for common workflows (coming soon)

### Hooks
Event-driven customizations for Claude behavior (coming soon)

## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ccconfig.git
   ```

2. Browse available agents in the `/agents` directory. Each agent is a markdown file with:
   - Metadata (name, description, tags) in the frontmatter
   - Detailed overview and use cases
   - Complete system prompt defining the agent's behavior
   - Real-world examples showing how to interact with the agent

3. To use an agent like `code-reviewer`:
   - Open `/agents/code-reviewer.md` to see its capabilities
   - Reference the agent by its name (`code-reviewer`) in your Claude workflow
   - The agent will behave according to its defined system prompt
   - Check the examples section to understand expected inputs and outputs

4. Customize or create new configurations following the existing patterns

## Creating New Configurations

### Adding an Agent

1. Create a new markdown file in `/agents/` directory
2. Follow this template:
   ```markdown
   ---
   name: your-agent-name
   description: Brief description of what this agent does
   color: purple
   ---
   
   Your agent's system prompt goes here...
   ```

### Adding Commands and Hooks

Documentation for commands and hooks will be added as these features are implemented.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Add your configuration following existing patterns
4. Submit a pull request with clear description

## Documentation

- [Requirements Specification](docs/claude-config-repo/requirements.md) - Detailed user stories and acceptance criteria

## License

This project is open source and available under the MIT License.