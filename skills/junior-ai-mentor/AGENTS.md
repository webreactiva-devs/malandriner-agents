# Junior AI Mentor Guidelines

> Compiled guidelines for AI coding agents mentoring junior developers. This document provides comprehensive guidance on AI-assisted development for newcomers to the field.

**Version:** 1.0.0
**Last Updated:** 2025-01-26

---

## Table of Contents

1. [Core Philosophy](#core-philosophy)
2. [AI Tool Types](#ai-tool-types)
3. [Vibe Coding Methodology](#vibe-coding-methodology)
4. [The 5 Mandatory Checkpoints](#the-5-mandatory-checkpoints)
5. [Common Mistakes](#common-mistakes)
6. [Security Considerations](#security-considerations)
7. [Career Development](#career-development)
8. [Prompting Guidelines](#prompting-guidelines)

---

## Core Philosophy

### The Golden Rule

**Never use code you can't explain.**

AI is a skill multiplier, not a replacement. A junior who understands fundamentals and uses AI intentionally outperforms someone who copies without understanding.

### Key Principles

| Principle | Meaning |
|-----------|---------|
| AI amplifies | It makes your existing skills more powerful |
| You're responsible | AI suggests, you decide and own the result |
| Understanding first | Learn what code does before shipping it |
| Fundamentals matter | AI helps experts more than beginners |

---

## AI Tool Types

### Autocomplete Tools

**Examples:** GitHub Copilot, Codeium, Supermaven

**Best for:**
- Repetitive code
- Boilerplate
- Known patterns

**Risks:**
- Accepting suggestions without review
- Over-reliance on autocomplete

**Usage advice:**
- Read every suggestion before accepting
- Use Tab judiciously
- Maintain your understanding

### Chat + Code Tools

**Examples:** Cursor, Claude Code, Windsurf

**Best for:**
- Complete features
- Refactoring
- Debugging

**Risks:**
- Losing track of changes
- Context confusion

**Usage advice:**
- Work incrementally
- Commit frequently
- Review all changes before accepting

### Autonomous Agents

**Examples:** Claude Code agents, Devin

**Best for:**
- Well-defined tasks
- Migrations
- Test generation

**Risks:**
- Unexpected changes
- Unsupervised modifications

**Usage advice:**
- Define clear boundaries
- Review all changes
- Use version control as safety net

---

## Vibe Coding Methodology

### Phase 1: Planning

1. Work with AI to write implementation plan in markdown
2. Review and refine—delete unnecessary items
3. Mark complex features as "won't do"
4. Keep separate section for future ideas

### Phase 2: Implementation

1. Work section by section
2. Mark sections complete after implementation
3. Commit each working section to git
4. Don't move forward until current section works

### Phase 3: Version Control

**Clean slate principle:**
- Start each feature with clean git state
- Use `git reset --hard HEAD` when stuck
- Don't layer failed attempts

**Clean implementation:**
- When solution found after many attempts
- Reset to clean state
- Implement fresh without accumulated mess

### Phase 4: Testing

**Prioritize:**
- End-to-end integration tests
- User behavior simulation
- Regression prevention

**Tests as guardrails:**
- Start with test cases when possible
- Tests define what AI should/shouldn't change
- Catch unintended modifications

---

## The 5 Mandatory Checkpoints

After receiving AI-generated code, verify:

| # | Question | Action if No |
|---|----------|--------------|
| 1 | Does it work? | Run it, don't assume |
| 2 | Do you understand every line? | Ask for explanation |
| 3 | Does it handle errors? | Check edge cases |
| 4 | Is it secure? | Review for vulnerabilities |
| 5 | Does it follow project style? | Adapt naming/structure |

### Checkpoint Details

**1. Does it work?**
- Actually run the code
- Test the happy path
- Don't trust "this should work"

**2. Do you understand every line?**
- If you see unfamiliar syntax, ask
- "Why useCallback instead of regular function?"
- No shame in asking

**3. Does it handle errors?**
- What if input is null?
- What if API fails?
- What if user does unexpected thing?

**4. Is it secure?**
- Check user input validation
- Look for hardcoded secrets
- Verify query parameterization
- Check dependency versions

**5. Does it follow project style?**
- Naming conventions
- File structure
- Patterns used elsewhere in codebase

---

## Common Mistakes

| Mistake | Consequence | Solution |
|---------|-------------|----------|
| Copy without understanding | Technical debt, hidden bugs | Ask for explanation before using |
| Vague prompts | Generic, unusable code | Give project-specific context |
| Not testing | Bugs in production | Always run and test edge cases |
| Ignoring warnings | Vulnerabilities, deprecations | Ask about every warning |
| Over-relying on one tool | Suboptimal solutions | Compare multiple sources |
| Layering failed fixes | Accumulated mess | Reset and implement clean |

### Anti-Pattern Examples

**Vague prompt:**
```
BAD: "Make a login"
```

**Specific prompt:**
```
GOOD: "I need JWT authentication for an Express API.
- Endpoint POST /auth/login
- Validate email and password against PostgreSQL
- Return token with 24h expiration
- Project already uses bcrypt for passwords"
```

---

## Security Considerations

### What AI Often Misses

| Issue | Risk | Manual Check |
|-------|------|--------------|
| User input validation | XSS, injection | Verify all inputs sanitized |
| Hardcoded secrets | Credential exposure | Search for API keys, passwords |
| SQL/NoSQL injection | Data breach | Check query parameterization |
| Outdated dependencies | Known vulnerabilities | Verify package versions |

### Security Review Prompt

```
"Review this code specifically for OWASP Top 10 vulnerabilities.
Is there any unvalidated or unsanitized input?"
```

### Pre-Commit Checklist

- [ ] No hardcoded secrets
- [ ] All user inputs validated
- [ ] Queries use parameterization
- [ ] Dependencies are current
- [ ] Error messages don't leak info

---

## Career Development

### Skills Gaining Value

1. **Systems thinking** - Designing architectures, not just functions
2. **Deep debugging** - AI helps, but you diagnose
3. **Critical code review** - Evaluating quality of any code
4. **Technical communication** - Good prompts = clear problem explanation
5. **Domain expertise** - Understanding WHAT to build

### Skills in Decline

- Memorizing syntax (AI remembers for you)
- Writing boilerplate (AI generates it)
- Searching Stack Overflow (AI searches for you)

### Your Competitive Advantage

| Advantage | How to Leverage |
|-----------|-----------------|
| Learn faster | Use AI for personalized explanations |
| Iterate faster | Prototype in minutes, not days |
| Explore more | Try ideas without high cost |

**But remember:** Solid fundamentals let you know when AI is wrong.

### Interview Strategy

| Context | Recommendation |
|---------|----------------|
| Personal projects | Use AI freely |
| Technical interviews | Ask if allowed first |
| At work | Be transparent with team |

---

## Prompting Guidelines

### Prompt Structure

```
[CONTEXT] - Technologies, project location
[OBJECTIVE] - What you want (outcome, not steps)
[CONSTRAINTS] - Limitations, conventions, what NOT to do
[FORMAT] - How you want the response
```

### Pre-Prompt Checklist

- [ ] Defined what I want to achieve (not how)
- [ ] Mentioned existing technologies/libraries
- [ ] Specified project constraints or conventions

### While AI Generates

1. Read in chunks, not all at once
2. Understand general structure first
3. Identify unfamiliar parts
4. Ask about what you don't understand

### Pattern Library

See `references/prompt-patterns.md` for:
- Context-first prompting
- Phased interaction
- Iterative refinement
- Example-driven prompting
- Validation-oriented prompting
- Emergency prompts

---

## Quick Reference Card

| Situation | Action |
|-----------|--------|
| Receiving AI code | Run 5 checkpoints |
| Vague task | Write detailed prompt with context |
| Stuck debugging | Reset, try different model |
| Security concern | Run OWASP review prompt |
| Multiple failures | Git reset, implement clean |
| Learning new concept | Ask AI to explain like you're junior |

---

## Tool Selection Guide

| Need | Recommended Tool |
|------|------------------|
| Learning new language | ChatGPT or Claude (chat) |
| Repetitive code | Copilot or Codeium |
| Complete features | Cursor or Claude Code |
| Automation tasks | Claude Code agents |

See `references/tools-comparison.md` for detailed comparison.

---

*Built for junior developers navigating the AI era.*
