# Claude Configuration Repository

A centralized repository for managing Claude AI configurations including agents, commands, and hooks.

## Overview

This repository serves as a collection of reusable Claude AI configurations to enhance developer productivity and enable consistent AI-powered workflows. It follows a spec-driven development approach with clear structure and documentation.

## Repository Structure

```
ccconfig/
├── .claude/                        # Claude AI configurations
│   ├── agents/                     # AI agent configurations
│   │   ├── README.md               # Agent system documentation
│   │   ├── requirements-analyst.md # Gathers user requirements
│   │   ├── system-architect.md     # Creates technical designs
│   │   ├── agile-task-decomposer.md # Breaks down into tasks
│   │   ├── task-executor.md        # Implements tasks
│   │   ├── code-reviewer.md        # Reviews code quality
│   │   ├── spec-driven-development.md # Main workflow orchestrator
│   │   ├── dev-accelerator.md      # Smart development shortcuts
│   │   ├── project-dashboard.md    # Project visibility & analytics
│   │   └── workflow-validator.md   # Quality assurance
│   ├── commands/                   # Slash commands
│   │   ├── spec.md                 # Full workflow command
│   │   ├── dev.md                  # Development shortcuts
│   │   ├── status.md               # Project monitoring
│   │   ├── validate.md             # Quality validation
│   │   └── spec/                   # Sub-commands
│   │       ├── requirements.md     # Requirements gathering
│   │       ├── design.md           # Technical design
│   │       ├── tasks.md            # Task creation
│   │       └── implement.md        # Task implementation
│   └── settings.local.json         # Local settings
├── hooks/                          # Event-driven hooks
├── docs/                           # Project documentation
│   └── claude-config-repo/         # This project's specs
│       ├── requirements.md
│       ├── design.md
│       └── tasks.md
└── examples/                       # Usage examples
    └── README.md
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

2. Browse available agents in the `/.claude/agents` directory. Each agent is a markdown file with:
   - Metadata (name, description, tags) in the frontmatter
   - Detailed overview and use cases
   - Complete system prompt defining the agent's behavior
   - Real-world examples showing how to interact with the agent

3. To use an agent like `code-reviewer`:
   - Open `/.claude/agents/code-reviewer.md` to see its capabilities
   - Reference the agent by its name (`code-reviewer`) in your Claude workflow
   - The agent will behave according to its defined system prompt
   - Check the examples section to understand expected inputs and outputs

4. Customize or create new configurations following the existing patterns

## Creating New Configurations

### Adding an Agent

1. Create a new markdown file in `/.claude/agents/` directory
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

## Code Quality

This project uses [LineGuard](https://github.com/hydai/lineguard) to ensure consistent line endings and clean formatting across all files. LineGuard checks are automatically run on all pull requests and pushes to the main branch.

### Running LineGuard Locally

To check your files before committing:
```bash
# Install LineGuard
cargo install lineguard

# Run checks
lineguard .

# Fix issues automatically
lineguard --fix .
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Add your configuration following existing patterns
4. Ensure your code passes LineGuard checks (`lineguard .`)
5. Submit a pull request with clear description

## Documentation

- [Requirements Specification](docs/claude-config-repo/requirements.md) - Detailed user stories and acceptance criteria

## License

This project is open source and available under the Apache License 2.0.
