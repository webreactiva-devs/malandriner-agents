# Junior AI Mentor Skill

> Practical guide for junior developers who want to leverage AI as a professional tool. Master vibe coding, prompt patterns, and build your career in the AI era.

[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Compatible-blue)](https://agentskills.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](../../LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-brightgreen)]()

## Overview

This skill transforms your AI coding assistant into a mentor specifically focused on helping junior developers navigate the AI-assisted development landscape. It covers:

- **Tool Selection** - Choose the right AI tool for your task
- **Vibe Coding** - Code by feel with AI, but do it right
- **Prompt Engineering** - Write prompts that get useful code
- **Security Awareness** - Catch what AI misses
- **Career Growth** - Build skills that matter in the AI era

### Key Capabilities

- **AI Tool Guidance** - Compare Copilot, Cursor, Claude Code, and more
- **Vibe Coding Methodology** - Plan, implement, test, commit
- **Prompt Patterns** - Learn what makes prompts effective
- **Code Review Skills** - Evaluate AI-generated code critically
- **Career Strategy** - Understand which skills to develop

## Installation

### Using npx (Recommended)

```bash
npx skills add https://github.com/delineas/malandriner-agents --skill junior-ai-mentor
```

### Manual Installation

```bash
git clone https://github.com/delineas/malandriner-agents.git
cp -r malandriner-agents/skills/junior-ai-mentor ~/.claude/skills/
```

## Usage

The skill activates when you're asking about AI-assisted development, tool selection, or junior developer concerns.

### Trigger Phrases

- "How do I use AI for coding?"
- "Copilot vs Cursor" or any tool comparison
- "How to write good prompts"
- "Vibe coding"
- "Is AI-generated code safe?"
- "What skills should I learn?"
- "How does AI affect my career?"

### Example Prompts

```
I'm a junior developer. How should I use Copilot without becoming dependent on it?
```

```
Help me write a better prompt for generating a REST API endpoint
```

```
I keep copying AI code without understanding it. How do I break this habit?
```

```
What should I learn to stay relevant as AI gets better at coding?
```

## Directory Structure

```
junior-ai-mentor/
├── SKILL.md              # Main skill instructions
├── README.md             # This documentation file
├── AGENTS.md             # Compiled guidelines for agents
└── references/           # Detailed reference documentation
    ├── tools-comparison.md   # AI tool comparison guide
    └── prompt-patterns.md    # Advanced prompting patterns
```

## Core Philosophy

**Golden rule**: Never use code you can't explain.

AI is a skill multiplier, not a replacement. A junior who:
- Understands fundamentals
- Uses AI intentionally
- Reviews critically
- Tests thoroughly

...outperforms someone who just copies and pastes.

## The 5 Mandatory Checkpoints

After receiving AI-generated code:

1. **Does it work?** - Run it, don't assume
2. **Do you understand every line?** - If not, ask
3. **Does it handle errors?** - Edge cases, invalid inputs
4. **Is it secure?** - Check for OWASP Top 10
5. **Does it follow project style?** - Naming, structure

## Reference Documentation

### Tools Comparison (`references/tools-comparison.md`)

Covers when to use each type of AI tool:
- **Autocomplete** (Copilot, Codeium) - For repetitive code
- **Chat + Code** (Cursor, Claude Code) - For complete features
- **Autonomous Agents** - For well-defined tasks

### Prompt Patterns (`references/prompt-patterns.md`)

Advanced prompting strategies:
- Context-first prompting
- Phased interaction
- Iterative refinement
- Example-driven prompting
- Validation-oriented prompting

## Career Guidance

### Skills Gaining Value

1. Systems thinking
2. Deep debugging
3. Critical code review
4. Technical communication
5. Domain expertise

### Your Competitive Advantage

Today's juniors have access to tools seniors didn't have:
- Learn faster with personalized explanations
- Iterate faster with rapid prototyping
- Explore more without high cost

But solid fundamentals are essential to know when AI is wrong.

## Compatibility

| Agent | Status |
|-------|--------|
| Claude Code | Fully supported |
| Cursor | Fully supported |
| Cline | Fully supported |
| OpenAI Codex | Compatible |
| GitHub Copilot | Compatible |
| Windsurf | Compatible |

## Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Make your changes
3. Submit a pull request

### Adding a New Reference

1. Create a new `.md` file in `references/`
2. Add the reference to `SKILL.md`
3. Update this README

## License

MIT License - see [LICENSE](../../LICENSE) for details.

## Resources

- [Agent Skills Specification](https://agentskills.io/specification)
- [Skills.sh Directory](https://skills.sh)

---

Built for junior developers navigating the AI era.

Made by [Dani Primo](https://webreactiva.com) — [@webreactiva-devs](https://github.com/webreactiva-devs)
