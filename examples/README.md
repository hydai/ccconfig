# Agent System Examples

This directory contains examples demonstrating how the spec-driven development agents work together. These are for reference only and should not be confused with actual project features.

## Example Workflows

### 1. Basic Authentication Feature
Shows how agents collaborate to build a login system:
- Requirements gathering with user stories
- Technical design with JWT architecture
- Task breakdown following INVEST principles
- Implementation with validation

### 2. Shopping Cart Feature
Demonstrates handling complex dependencies:
- Multi-actor requirements (customer, admin)
- Microservice architecture design
- Parallel task execution strategies

### 3. Payment Integration
Illustrates external integration patterns:
- Compliance requirements handling
- Third-party API design patterns
- Risk-based task prioritization

## How Agents Communicate

The agents pass information through structured documents:

```
requirements-analyst → requirements.md → system-architect
                                     ↓
task-executor ← tasks.md ← agile-task-decomposer ← design.md
```

Each agent:
1. Reads outputs from previous agents
2. Validates inputs match expected format
3. Produces outputs for next agent
4. Updates status for tracking

## Running Examples

These examples are for learning purposes. To actually use the agents:

1. **Start fresh**: `/spec [feature-name]`
2. **Continue work**: `/dev [feature-name]`
3. **Check status**: `/status [feature-name]`
4. **Validate quality**: `/validate [feature-name]`

## Key Patterns Demonstrated

### Sequential Handoff
Each agent completes its phase before the next begins, ensuring proper information flow.

### Validation Gates
The workflow validator checks artifacts between stages to prevent errors from propagating.

### Smart Navigation
The dev accelerator detects the current stage and invokes the appropriate next agent.

### Parallel Coordination
Multiple agents can work on different features simultaneously without interference.

## Best Practices Shown

1. **Clear Boundaries**: Each agent has a specific responsibility
2. **Structured Communication**: Standardized document formats
3. **Traceability**: Requirements tracked through implementation
4. **Quality Focus**: Validation at each stage
5. **User Value**: Every task delivers visible progress