---
name: junior-ai-mentor
description: |
  Mentor for junior developers on AI in programming. Guide for using code assistants (Copilot, Cursor, Claude Code), AI agents, and effective vibe coding.

  Use when a junior developer asks about: how to use AI for coding, which AI tool to choose, how to write good prompts for code, vibe coding, pair programming with AI, how AI affects their career, what skills to develop in the AI era, common mistakes when using AI for code, how to review AI-generated code, or when they mention Copilot, Cursor, Claude Code, ChatGPT for programming.
license: MIT
metadata:
  author: delineas
  version: "1.0.0"
  category: mentorship
  tags: junior, ai-development, copilot, cursor, claude-code, vibe-coding
---

# Junior AI Mentor

Practical guide for junior developers who want to leverage AI as a professional tool.

## Core Philosophy

AI is a skill multiplier, not a replacement. A junior who understands fundamentals + uses AI well outperforms someone who just copies code without understanding it.

**Golden rule**: Never use code you can't explain. AI accelerates, but you build the understanding.

## Types of AI Tools

### Autocomplete (Copilot, Codeium, Supermaven)
- Suggest code as you type
- Best for: repetitive code, boilerplate, known patterns
- Risk: accepting suggestions without review

### Chat + Code (Cursor, Claude Code, Windsurf)
- Conversation + file editing
- Best for: complete features, refactoring, debugging
- Risk: losing track of what changed

### Autonomous Agents (Claude Code agents, Devin)
- Execute multi-step tasks autonomously
- Best for: well-defined tasks, migrations, tests
- Risk: unexpected changes without supervision

## Effective Vibe Coding Methodology

### Planning Phase

Start by working with the AI to write a detailed implementation plan in a markdown file.

**Scope management**: Review and refine the plan—delete unnecessary items, mark complex features as "won't do," and keep a separate section for ideas to implement later. This prevents scope creep.

**Incremental implementation**: Work section by section. Have the AI mark sections complete after implementation, and commit each working section to git before moving to the next.

### Version Control as Safety Net

Git is your safety net—don't rely solely on the AI tool's revert functionality.

**Clean slate principle**: Begin each new feature with a clean git state. When stuck, use `git reset --hard HEAD` if the AI goes down an unproductive path.

**Clean implementation**: When you finally find a working solution after several attempts, reset to a clean state and implement it fresh. Multiple failed attempts create layers of bad code—don't keep the accumulated mess.

### The Testing Imperative

Prioritize end-to-end integration tests over unit tests. Focus on simulating user behavior.

**Regression prevention**: LLMs often make unnecessary changes to unrelated logic. Tests catch these before they compound.

**Tests as guardrails**: Consider starting with test cases to provide clear boundaries for what the AI should and shouldn't change.

### Prompting Best Practices

**Before asking for code:**
```
BAD:  "Make a login"
GOOD: "I need JWT authentication for an Express API.
      - Endpoint POST /auth/login
      - Validate email and password against PostgreSQL
      - Return token with 24h expiration
      - Project already uses bcrypt for passwords"
```

**Pre-prompt checklist:**
- [ ] Defined what I want to achieve (not how)
- [ ] Mentioned existing technologies/libraries
- [ ] Specified project constraints or conventions

### While AI Generates

Don't accept everything at once. Read in chunks:
1. First understand the general structure
2. Identify parts you don't recognize
3. Ask about what you don't understand

```
"Explain why you used useCallback here
instead of a regular function"
```

### The 5 Mandatory Checkpoints

After receiving code:

1. **Does it work?** - Run it, don't assume
2. **Do you understand every line?** - If not, ask
3. **Does it handle errors?** - Edge cases, invalid inputs
4. **Is it secure?** - See security section
5. **Does it follow project style?** - Naming, structure

### Bug Fixing with AI

**Error messages**: Copy-pasting error messages is often enough context.

**Analyze before coding**: Ask the AI to consider multiple possible causes before jumping to implementation.

**Reset after failures**: Start with a clean slate after each unsuccessful fix rather than layering fixes.

**Strategic logging**: Add logging statements when bugs are opaque.

**Switch models**: Try different AI models when one gets stuck.

## AI Tool Optimization

**Instruction files**: Write detailed instructions in project files (cursor.rules, windsurf.rules, CLAUDE.md). These provide project-specific context.

**Local documentation**: Download API docs to your project folder. AI tools work more accurately with local docs.

**Multiple tools**: Some developers run both Cursor and Windsurf on the same project. Different tools excel at different tasks.

**Compare outputs**: Generate multiple solutions and pick the best one.

## Common Junior Mistakes with AI

| Mistake | Consequence | Solution |
|---------|-------------|----------|
| Copy without understanding | Technical debt, hidden bugs | Ask for explanation before using |
| Vague prompts | Generic code that doesn't apply | Give project-specific context |
| Not testing | Bugs in production | Always run and test edge cases |
| Ignoring warnings | Vulnerabilities, deprecations | Ask about every warning |
| Over-relying on one tool | Suboptimal solutions | Compare responses from multiple sources |
| Layering failed fixes | Accumulated mess | Reset and implement clean |

## Security: What AI Can Miss

**Always verify manually:**

- **User inputs**: AI may forget to sanitize
- **Hardcoded secrets**: May include example API keys
- **SQL/NoSQL injection**: Concatenated queries without parameterization
- **Dependencies**: May suggest outdated or malicious packages

```
Security prompt:
"Review this code specifically for OWASP Top 10
vulnerabilities. Is there any unvalidated or unsanitized input?"
```

## Building Your Career with AI

### Skills Gaining Value

1. **Systems thinking** - Designing architectures, not just functions
2. **Deep debugging** - AI helps, but you diagnose
3. **Critical code review** - Evaluating code quality (human or AI)
4. **Technical communication** - Writing good prompts = explaining problems clearly
5. **Domain expertise** - Understanding WHAT to build, not just HOW

### Skills in Decline (but still useful)

- Memorizing syntax
- Writing boilerplate from scratch
- Searching Stack Overflow for common errors

### Your Competitive Advantage

Today's juniors have access to tools seniors didn't have. Your advantage is:

1. **Learn faster** - Personalized explanations instantly
2. **Iterate faster** - Prototypes in minutes, not days
3. **Explore more** - Try ideas without high cost

But you need: **solid fundamentals** to know when AI is wrong.

## Beyond Just Coding

AI assistants help with more than writing code:

- **DevOps**: Configuring servers, DNS, hosting
- **Design**: Generating favicons and design elements
- **Documentation**: Drafting docs and materials
- **Education**: Explaining implementations line by line
- **Visual input**: Share screenshots for UI bugs or inspiration
- **Voice input**: Tools like Aqua enable faster input

## For Interviews and Portfolio

### Using AI in Personal Projects: Yes
- Accelerates your learning
- Lets you build more ambitious things
- Shows you use modern tools

### In Technical Interviews: Depends
- Ask if it's allowed first
- If not, solve alone to demonstrate fundamentals
- You can mention: "In my daily work I use X for Y"

### At Work: Transparency
- Inform your team that you use AI
- The code is your responsibility, regardless of who generated it
- Document important decisions, not just code

## Tech Stack Considerations

**Established frameworks**: Ruby on Rails and similar mature frameworks work well due to consistent conventions in training data.

**Training data matters**: Newer languages may have less training data, leading to more errors.

**Modularity**: Small, modular files work better than files with thousands of lines—they exceed context windows.

## Continuous Improvement

**Regular refactoring**: Once tests are in place, refactor frequently. Ask AI to identify candidates.

**Stay current**: Try every new model release. Different models excel at different tasks.

## Additional Resources

For detailed guides:
- `references/tools-comparison.md` - Code assistant comparison
- `references/prompt-patterns.md` - Advanced prompt patterns
