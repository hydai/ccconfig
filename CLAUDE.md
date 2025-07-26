# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the Claude Configuration Repository (ccconfig) - a collection of reusable AI agent configurations, commands, and hooks that implement a comprehensive spec-driven development workflow. The repository enables teams to transform ideas into working software through coordinated AI agents.

## Commands

### Code Quality
```bash
# Run LineGuard to check and fix line endings/formatting
lineguard .
lineguard --fix .
```

### Git Workflow
```bash
# The repository follows conventional commits
# Format: type(scope): description
# Types: feat, fix, docs, style, refactor, test, chore
git commit -m "feat: add new agent configuration"
```

## High-Level Architecture

### Agent Orchestration System

The repository implements a spec-driven development methodology through coordinated agents:

1. **Sequential Workflow**: Requirements → Design → Tasks → Implementation
2. **Agent Communication**: Agents communicate through structured markdown documents in `docs/[feature]/`
3. **Validation Gates**: Each stage validates outputs from the previous stage before proceeding
4. **Smart Navigation**: The dev-accelerator agent detects current state and routes to appropriate next steps

### Core Agent Roles

- **requirements-analyst**: Transforms ideas into numbered User Stories with Gherkin acceptance criteria
- **system-architect**: Creates technical designs with architecture diagrams and interface contracts
- **agile-task-decomposer**: Breaks designs into INVEST-compliant, value-driven tasks
- **task-executor**: Implements tasks following TDD with validation against requirements

### Orchestration Agents

- **spec-driven-development**: Main workflow orchestrator managing handoffs and quality gates
- **dev-accelerator**: Provides intelligent shortcuts and automation
- **project-dashboard**: Offers comprehensive project visibility and analytics
- **workflow-validator**: Ensures quality and consistency at every stage

### Configuration Structure

All Claude configurations live under `.claude/`:
- `.claude/agents/`: Agent definitions with system prompts and behaviors
- `.claude/commands/`: Slash commands for easy agent invocation
- `.claude/settings.local.json`: Local Claude settings

### Document Flow

Agents produce and consume documents in a specific format:
```
docs/[feature]/
├── requirements.md    # User stories with acceptance criteria
├── design.md         # Technical architecture and interfaces
├── tasks.md          # Implementation tasks with status tracking
└── traceability.md   # Requirements to implementation mapping
```

## Key Development Patterns

### Creating New Agents

1. Agents must follow the frontmatter format:
   ```markdown
   ---
   name: agent-name
   description: Brief description
   version: 1.0.0
   author: username
   tags: [tag1, tag2]
   color: blue
   ---
   ```

2. Include comprehensive system prompt defining behavior
3. Provide real-world examples showing usage
4. Place in `.claude/agents/` directory

### Adding Slash Commands

1. Create markdown file in `.claude/commands/`
2. Reference agents using `@.claude/agents/[agent-name].md`
3. Support arguments with `$ARGUMENTS` placeholder
4. Can create sub-commands in nested directories

### Workflow Integration

When implementing features:
1. Start with `/spec [feature]` for full workflow
2. Use `/dev` for smart navigation to next steps
3. Check progress with `/status`
4. Validate quality with `/validate`

The agents automatically handle information passing through the docs directory structure, maintaining context and ensuring each stage builds on the previous one.

## Project Status

The repository has implemented:
- Complete spec-driven development agent system
- Orchestration for multi-agent workflows
- Slash commands for easy invocation
- Example documentation and usage patterns
- LineGuard integration for code quality

Current task completion (from docs/claude-config-repo/tasks.md):
- Task 1: ✅ Basic repository structure with code-reviewer agent
- Tasks 2-15: Pending implementation