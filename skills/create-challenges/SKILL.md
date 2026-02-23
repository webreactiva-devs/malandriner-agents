---
name: create-challenges
description: Transform learning content (transcripts, articles, tutorials) into a series of bite-sized, actionable challenges. Each challenge has 3-5 simple steps max. Use when user wants to "create challenges", "make this a challenge", "turn into mini-challenges", "create a challenge series", "reto", "desafío", or wants quick actionable tasks from educational content.
allowed-tools:
  - Read
  - Write
  - Bash
  - WebSearch
---

# Create Challenges

Transform passive learning content into a series of **bite-sized challenges** - small, actionable tasks that can be completed quickly.

## Core Philosophy

- **Simplicity over completeness**: Each challenge should be doable in 1-3 hours max
- **3-5 steps only**: No more than 5 action steps per challenge
- **Immediate action**: User should be able to start right now
- **Progressive complexity**: Each challenge builds on the previous, increasing difficulty
- **Reflect to improve**: Brief reflection after each challenge to consolidate learning

## Workflow

### Step 1: Read the Content

Read the file the user provides using the Read tool.

### Step 2: Extract Key Lessons

Identify 3-7 actionable concepts from the content. Focus on:
- Techniques that can be practiced immediately
- Concrete skills, not abstract theory
- Things that produce a tangible result

### Step 3: Create Challenges

For each key lesson, create ONE challenge with:
- A clear, specific goal
- 3-5 simple action steps (NO MORE)
- A concrete deliverable

**Keep it simple. If a challenge needs more than 5 steps, split it into two challenges.**

### Step 4: Search for Resources

Use WebSearch to find relevant resources:
1. Search in **English** for the topic
2. Search in the **user's prompt language** for localized resources
3. Collect 5-10 useful links total

## Language Adaptation

**CRITICAL**: The output document MUST be written in the same language as the user's request.

**Title casing rules**:
- **Spanish**: Sentence case (only first letter capitalized)
  - "# Retos: Aprender TypeScript"
  - "## Reto 1: Tu primer tipo"
- **English**: Title Case
  - "# Challenges: Learn TypeScript"
  - "## Challenge 1: Your First Type"
- **Other languages**: Follow that language's conventions

## Output Structure

### English Template

```markdown
# Challenges: [Topic]

**Source**: [Content title/file]
**Key takeaways**: [2-3 bullet points]

---

## Challenge 1: [Specific Goal]

**Difficulty**: ⭐ Beginner
**Builds on**: Nothing (starting point)

**Do this**: [One sentence description]

**Steps**:
1. [Simple step]
2. [Simple step]
3. [Simple step]

**Done when**: [Clear completion criteria]

**Reflect**:
- What worked well?
- What was harder than expected?

---

## Challenge 2: [Next Goal]

**Difficulty**: ⭐⭐ Easy
**Builds on**: Challenge 1

**Do this**: [One sentence description]

**Steps**:
1. [Simple step]
2. [Simple step]
3. [Simple step]

**Done when**: [Clear completion criteria]

**Reflect**:
- What did you learn from Challenge 1 that helped here?
- What would you do differently?

---

## Challenge 3: [Next Goal]

**Difficulty**: ⭐⭐⭐ Intermediate
**Builds on**: Challenges 1-2

...

---

[Continue for 3-7 challenges with increasing difficulty]

---

## Resources

### English
- [Resource title](url) - Brief description
- [Resource title](url) - Brief description

### [User's language]
- [Resource title](url) - Brief description
- [Resource title](url) - Brief description
```

### Spanish Template (Sentence case)

```markdown
# Retos: [Tema]

**Fuente**: [Título del contenido/archivo]
**Ideas clave**: [2-3 puntos]

---

## Reto 1: [Objetivo específico]

**Dificultad**: ⭐ Principiante
**Construye sobre**: Nada (punto de partida)

**Haz esto**: [Descripción en una frase]

**Pasos**:
1. [Paso simple]
2. [Paso simple]
3. [Paso simple]

**Completado cuando**: [Criterio claro de finalización]

**Reflexiona**:
- ¿Qué funcionó bien?
- ¿Qué fue más difícil de lo esperado?

---

## Reto 2: [Siguiente objetivo]

**Dificultad**: ⭐⭐ Fácil
**Construye sobre**: Reto 1

**Haz esto**: [Descripción en una frase]

**Pasos**:
1. [Paso simple]
2. [Paso simple]
3. [Paso simple]

**Completado cuando**: [Criterio claro de finalización]

**Reflexiona**:
- ¿Qué aprendiste del Reto 1 que te ayudó aquí?
- ¿Qué harías diferente?

---

## Reto 3: [Siguiente objetivo]

**Dificultad**: ⭐⭐⭐ Intermedio
**Construye sobre**: Retos 1-2

...

---

[Continuar para 3-7 retos con dificultad creciente]

---

## Recursos

### En inglés
- [Título del recurso](url) - Breve descripción
- [Título del recurso](url) - Breve descripción

### En español
- [Título del recurso](url) - Breve descripción
- [Título del recurso](url) - Breve descripción
```

## Challenge Design Rules

**DO**:
- Make each step a single, clear action
- Use concrete verbs: "Create", "Write", "Build", "Test"
- Include a tangible deliverable for each challenge
- Keep time estimates under 3 hours per challenge
- Add progressive difficulty (⭐ to ⭐⭐⭐⭐⭐)
- Include "Builds on" to show dependencies
- Add brief reflection questions (2 max) after each challenge

**DON'T**:
- Add "nice to have" steps
- Include setup/installation unless essential
- Make reflection too long (keep it to 2 questions max)
- Skip the difficulty indicator

## Saving the Document

### Directory
Save to `docs/challenges/`. Create if it doesn't exist:
```bash
mkdir -p docs/challenges
```

### Filename
- Lowercase slug, max 60 characters
- Format: `[topic-slug].md`

Examples:
- `docs/challenges/spec-driven-development.md`
- `docs/challenges/react-hooks.md`
- `docs/challenges/cold-outreach.md`

## Resource Search Strategy

After creating challenges, use WebSearch to find helpful resources:

**Search queries to run**:
1. `[topic] tutorial beginner` (English)
2. `[topic] getting started guide` (English)
3. `[topic] examples` (English)
4. `[translated topic] tutorial` (user's language)
5. `[translated topic] guía práctica` (user's language, if Spanish)

**Select resources that are**:
- Free and accessible
- Practical (tutorials > theory)
- Recent (prefer last 2 years)
- From reputable sources

**Include in final document**:
- 3-5 English resources
- 3-5 resources in user's language (if different from English)

## After Creating

1. Show: "Saved to: [filepath]"
2. Highlight Challenge 1 briefly
3. Ask: "Ready to start Challenge 1?"
