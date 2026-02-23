# Malandriner Agents

> Agent Skills for pragmatic, human-centered software development. Compatible with Claude Code, Cursor, Cline, OpenAI Codex, and other agents supporting the [Agent Skills specification](https://agentskills.io).

[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Compatible-blue)](https://agentskills.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

**[Subscribe to Web Reactiva Newsletter](https://webreactiva.com/newsletter)** — Weekly insights on web development, AI tools, and the Malandriner philosophy.

---

## The Malandriner Philosophy

The Malandriner Manifesto was born in the [Web Reactiva](https://webreactiva.com) community. It's a pragmatic, human-centered approach to software development in the AI era:

- **Hands on the keyboard** — Learning happens through practice, not theory
- **Level up like it's a game** — Make learning fun, celebrate small wins
- **Your stumbles, my challenges** — Every mistake becomes learning for all
- **Break the bad rules** — Build your own path, question dogma
- **Speak Malandriner** — Belong to a tribe that gets it

These skills bring this philosophy to your AI coding assistants.

---

## Available Skills

| Skill | Description | Install |
|-------|-------------|---------|
| [malandriner-developer](skills/malandriner-developer/) | Mentorship and guidance following the Malandriner Manifesto philosophy. Human-centered code reviews, AI-assisted development, and team culture practices. | `npx skills add https://github.com/webreactiva-devs/malandriner-agents --skill malandriner-developer` |
| [junior-ai-mentor](skills/junior-ai-mentor/) | Practical guide for junior developers leveraging AI as a professional tool. Covers vibe coding, prompt patterns, and career growth. | `npx skills add https://github.com/webreactiva-devs/malandriner-agents --skill junior-ai-mentor` |
| [build-your-path](skills/build-your-path/) | Transforms learning content into actionable Build-Do-Reflect iteration plans. Turns passive advice into concrete, buildable cycles over 4-8 weeks. | `npx skills add https://github.com/webreactiva-devs/malandriner-agents --skill build-your-path` |
| [create-challenges](skills/create-challenges/) | Transforms learning content into bite-sized, progressive challenges. Each challenge has 3-5 steps max and is completable in 1-3 hours. | `npx skills add https://github.com/webreactiva-devs/malandriner-agents --skill create-challenges` |

## Quick Start

### Install a Single Skill

```bash
npx skills add https://github.com/webreactiva-devs/malandriner-agents --skill malandriner-developer
```

### Manual Installation

Clone the repository and copy the desired skill folder to your agent's skills directory:

```bash
git clone https://github.com/webreactiva-devs/malandriner-agents.git
cp -r malandriner-agents/skills/malandriner-developer ~/.claude/skills/
```

## Repository Structure

```
malandriner-agents/
├── README.md                 # This file (repository index)
├── LICENSE                   # MIT License
├── .gitignore
└── skills/                   # All skills live here
    ├── README.md               # Skills index and comparison
    ├── malandriner-developer/  # Malandriner philosophy skill
    │   ├── SKILL.md            # Main skill instructions
    │   └── AGENTS.md           # Compiled guidelines
    ├── junior-ai-mentor/       # Junior AI mentorship skill
    │   ├── SKILL.md            # Main skill instructions
    │   ├── AGENTS.md           # Compiled guidelines
    │   └── references/         # Detailed reference docs
    │       ├── tools-comparison.md
    │       └── prompt-patterns.md
    ├── build-your-path/        # Learning-to-action planner
    │   └── SKILL.md            # Main skill instructions
    └── create-challenges/      # Bite-sized challenge creator
        └── SKILL.md            # Main skill instructions
```

## Creating a New Skill

1. Create a new directory under `skills/`:

```bash
mkdir -p skills/my-new-skill
```

2. Create the required `SKILL.md` with frontmatter:

```yaml
---
name: my-new-skill
description: Description of what this skill does and when to use it.
license: MIT
metadata:
  author: your-name
  version: "1.0.0"
---

# My New Skill

Instructions for the agent...
```

3. (Optional) Add supporting files:
   - `AGENTS.md` - Compiled guidelines for agents
   - `references/` - Detailed reference documentation

4. Update this README to include your new skill in the table.

## Skill Format Specification

Each skill follows the [Agent Skills Specification](https://agentskills.io/specification):

### Required Files

- `SKILL.md` - Main skill file with YAML frontmatter and instructions

### Required Frontmatter

```yaml
---
name: skill-name          # Must match directory name
description: "..."        # What it does and when to use it
---
```

### Optional Frontmatter

```yaml
---
license: MIT
metadata:
  author: your-name
  version: "1.0.0"
  category: mentorship
  tags: malandriner, web-reactiva, ai-development
---
```

### Optional Directories

| Directory | Purpose |
|-----------|---------|
| `references/` | Detailed documentation loaded on-demand |
| `rules/` | Context-specific rules with glob patterns |
| `scripts/` | Executable scripts the agent can run |
| `assets/` | Templates, images, data files |

## Compatibility

These skills are compatible with:

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
2. Create a new skill in `skills/your-skill-name/`
3. Follow the [Agent Skills Specification](https://agentskills.io/specification)
4. Add your skill to the table in this README
5. Submit a pull request

### Guidelines

- Keep `SKILL.md` under 500 lines (use `references/` for detailed docs)
- Use progressive disclosure (metadata -> instructions -> references)
- Include clear examples in your instructions
- Embrace the Malandriner philosophy: practical, human-centered, no gatekeeping

## License

MIT License - see [LICENSE](LICENSE) for details.

## Resources

- [Web Reactiva](https://webreactiva.com) - Home of the Malandriner Community
- [Web Reactiva Newsletter](https://webreactiva.com/newsletter) - Weekly insights
- [Agent Skills Specification](https://agentskills.io/specification)
- [Skills.sh Directory](https://skills.sh)

---

Built with love for the open web and the Malandriner Community of [Web Reactiva](https://webreactiva.com)

Made by [Dani Primo](https://webreactiva.com) — [@webreactiva-devs](https://github.com/webreactiva-devs)
