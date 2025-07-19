# Copilot Chat Modes Experiments

This repository contains experimental chat modes, instructions, and prompts for GitHub Copilot Chat to explore different AI assistant behaviors and capabilities.

## Repository Structure

```
copilot-experiments/
├── README.md                               # This file
├── chatmodes/                              # Chat mode personas
│   └── code-reviewer.chatmode.md          # Example: Code reviewer persona
├── instructions/                           # Instruction sets
│   └── secure-coding.instructions.md      # Example: Security-focused instructions
├── prompts/                               # Prompt templates
│   └── refactor-function.prompt.md        # Example: Function refactoring prompt
├── templates/                             # Templates for creating new files
│   ├── chatmode-template.chatmode.md      # Template for chat modes
│   ├── instructions-template.instructions.md # Template for instructions
│   └── prompt-template.prompt.md          # Template for prompts
└── experiments/                           # Experiment documentation
    └── README.md                          # Guide for documenting results
```

## File Naming Conventions

- **Chat Modes**: `<name>.chatmode.md` - Define AI assistant personas and behaviors
- **Instructions**: `<name>.instructions.md` - Provide specific instruction sets for tasks
- **Prompts**: `<name>.prompt.md` - Template prompts for common operations

## Usage

### Using Chat Modes
Chat modes define how the AI assistant should behave and respond. To use a chat mode:

1. Browse the `chatmodes/` directory
2. Copy the content from your desired `.chatmode.md` file
3. Paste it into your Copilot Chat session to set the AI's persona

### Using Instructions
Instructions provide specific guidance for particular types of tasks:

1. Browse the `instructions/` directory  
2. Copy the relevant `.instructions.md` content
3. Include it in your Copilot Chat prompt along with your specific request

### Using Prompts
Prompts are templates for common operations:

1. Browse the `prompts/` directory
2. Copy the template from a `.prompt.md` file
3. Customize the placeholders with your specific requirements
4. Send the completed prompt to Copilot Chat

### Creating New Content

Use the templates in the `templates/` directory as starting points:

- Copy `templates/chatmode-template.chatmode.md` to create new chat modes
- Copy `templates/instructions-template.instructions.md` to create new instruction sets  
- Copy `templates/prompt-template.prompt.md` to create new prompt templates

Follow the naming conventions and place files in the appropriate directories.

## Contributing

1. Create new chat modes, instructions, or prompts using the provided templates
2. Document your experiments in the `experiments/` directory
3. Share successful patterns and learnings with the community

## Experiments

See `experiments/README.md` for guidance on documenting your experimental results and sharing learnings with the community.
