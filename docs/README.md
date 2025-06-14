# Kilocode Documentation

Welcome to the Kilocode documentation! This directory contains comprehensive documentation for understanding, using, and contributing to the Kilocode agentic AI framework.

## 📚 Documentation Overview

### [Agentic Framework Documentation](./AGENTIC_FRAMEWORK.md)
The complete guide to Kilocode's agentic AI framework, covering:

- **Architecture Overview**: How the framework enables autonomous AI operation
- **Core Components**: Task planning, decision-making, tool integration, and feedback loops
- **Inner Loop Implementation**: Detailed explanation of autonomous execution patterns
- **Technical Implementation**: Code examples, API references, and architectural diagrams
- **Usage Examples**: Concrete examples of autonomous task completion
- **Advanced Features**: Context management, checkpoints, and MCP integration
- **Best Practices**: Guidelines for optimal framework usage
- **Troubleshooting**: Common issues and debugging techniques
- **Contributing**: How to extend and contribute to the framework

## 🏗️ Architecture Highlights

### Autonomous Inner Loop Pattern
Kilocode implements a sophisticated "inner loop" execution pattern that enables AI agents to:

1. **Receive and interpret** user tasks autonomously
2. **Break down complex tasks** into actionable steps
3. **Execute steps using available tools** without constant human intervention
4. **Monitor progress and adapt** when encountering obstacles
5. **Validate completion** and report results

### Key Components

#### 🎯 Mode System
- **Code Mode**: General-purpose development tasks
- **Architect Mode**: Planning and design-focused operations
- **Debug Mode**: Systematic problem diagnosis and resolution
- **Ask Mode**: Information gathering and question answering
- **Orchestrator Mode**: Complex workflow coordination

#### 🛠️ Tool System
Comprehensive tool integration enabling:
- **File Operations**: Reading, writing, and modifying files
- **Code Analysis**: Understanding and navigating codebases
- **Command Execution**: Running terminal commands and scripts
- **Web Automation**: Browser-based research and interaction
- **MCP Integration**: Extensible capabilities through external servers

#### 🔄 Feedback Mechanisms
- **Consecutive Mistake Detection**: Prevents infinite loops
- **Tool Repetition Detection**: Identifies and breaks repetitive patterns
- **Validation Systems**: Ensures code quality and functionality
- **User Approval Gates**: Maintains human oversight for critical operations

## 🚀 Quick Start

### Basic Usage
```typescript
// Create a new autonomous task
const task = new Task({
    context,
    provider,
    apiConfiguration,
    task: "Create a REST API for user management with CRUD operations",
    startTask: true
})

// The agent will autonomously:
// 1. Analyze the request
// 2. Plan the implementation
// 3. Create necessary files
// 4. Implement functionality
// 5. Add tests and validation
// 6. Report completion
```

### Mode-Specific Operations
```typescript
// Architecture planning
const architectTask = new Task({
    // ... configuration
    task: "Design a microservices architecture for an e-commerce platform",
    mode: "architect"
})

// Debugging workflow
const debugTask = new Task({
    // ... configuration
    task: "Debug and fix the failing tests in the user authentication module",
    mode: "debug"
})
```

## 🔧 Configuration

### Tool Groups and Permissions
```typescript
// Configure mode-specific tool access
const customMode: ModeConfig = {
    slug: "security-audit",
    name: "Security Audit",
    roleDefinition: "Security-focused code analysis specialist",
    groups: ["read", "browser"], // Restricted to read-only and research tools
    customInstructions: "Focus on identifying security vulnerabilities..."
}
```

### MCP Server Integration
```json
{
    "mcpServers": {
        "git": {
            "type": "stdio",
            "command": "npx",
            "args": ["-y", "@modelcontextprotocol/server-git", "--repository", "."]
        },
        "filesystem": {
            "type": "stdio",
            "command": "npx",
            "args": ["-y", "@modelcontextprotocol/server-filesystem", "/workspace"]
        }
    }
}
```

## 📊 Framework Benefits

### For Developers
- **Autonomous Operation**: Reduces manual intervention in routine tasks
- **Intelligent Planning**: Breaks down complex requirements automatically
- **Tool Integration**: Seamless access to development tools and services
- **Error Recovery**: Robust handling of failures and edge cases
- **Extensibility**: Easy integration of custom tools and capabilities

### For Teams
- **Consistent Quality**: Standardized approaches to common development tasks
- **Knowledge Sharing**: Captures and applies best practices automatically
- **Productivity Gains**: Accelerates development cycles through automation
- **Risk Mitigation**: Built-in validation and approval mechanisms

### For Organizations
- **Scalable Automation**: Framework scales from simple scripts to complex workflows
- **Compliance Support**: Audit trails and approval processes for sensitive operations
- **Integration Flexibility**: Works with existing tools and infrastructure
- **Cost Efficiency**: Reduces manual effort while maintaining quality standards

## 🔍 Key Concepts

### Inner Loop Execution
The framework's core innovation is its ability to operate in autonomous "inner loops" where the AI agent:
- Maintains context across multiple tool executions
- Makes intelligent decisions about next steps
- Recovers from errors and adapts strategies
- Validates progress and completion criteria

### Tool-Driven Architecture
All agent capabilities are exposed through a unified tool system that:
- Provides consistent interfaces for different operations
- Enables fine-grained permission control
- Supports dynamic capability extension through MCP
- Maintains audit trails for all operations

### Mode-Based Specialization
Different operational modes optimize agent behavior for specific scenarios:
- **Specialized Prompting**: Mode-specific system prompts and instructions
- **Tool Restrictions**: Appropriate tool access for each mode's purpose
- **Behavioral Optimization**: Tailored decision-making patterns
- **Context Awareness**: Mode-appropriate interpretation of user requests

## 📖 Further Reading

- **[Complete Framework Documentation](./AGENTIC_FRAMEWORK.md)**: Comprehensive technical guide
- **[API Reference](./AGENTIC_FRAMEWORK.md#api-reference)**: Detailed API documentation
- **[Usage Examples](./AGENTIC_FRAMEWORK.md#usage-examples)**: Practical implementation examples
- **[Contributing Guide](./AGENTIC_FRAMEWORK.md#contributing)**: How to extend the framework
- **[Troubleshooting](./AGENTIC_FRAMEWORK.md#troubleshooting)**: Common issues and solutions

## 🤝 Contributing

We welcome contributions to improve the Kilocode framework! Please see the [Contributing section](./AGENTIC_FRAMEWORK.md#contributing) in the main documentation for:

- Adding new tools
- Creating custom modes
- Extending MCP integration
- Improving documentation
- Reporting issues and bugs

## 📄 License

This documentation is part of the Kilocode project. Please refer to the main project license for usage terms and conditions.

---

*For the most up-to-date information and detailed technical specifications, please refer to the [complete framework documentation](./AGENTIC_FRAMEWORK.md).*
