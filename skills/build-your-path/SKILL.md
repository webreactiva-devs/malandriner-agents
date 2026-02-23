---
name: build-your-path
description: Transform learning content (YouTube transcripts, articles, tutorials, courses) into actionable implementation plans using the Build-Your-Path framework. Use when user wants to turn advice, lessons, or educational content into concrete action steps, iterations, or a learning journey. Triggers include "make this actionable", "turn this into a plan", "I watched/read X, now what?", "implement this advice", "create action steps from this", "build a learning path".
allowed-tools:
  - Read
  - Write
  - Bash
---

# Build-Your-Path Action Planner

Transform passive learning content into actionable **Build-Do-Reflect cycles** - turning advice and lessons into concrete, buildable iterations.

## Core Framework

Every learning journey follows three repeating phases:

1. **BUILD** - Create something real (code, content, product, demonstration)
2. **DO** - Execute and experience the process
3. **REFLECT** - Honest assessment of what happened, plan next iteration

**Key principle**: 100 iterations beats 100 hours of study. Learning = doing better, not knowing more.

## Workflow

### Step 1: Read the Content

Read the file the user provides (transcript, article, notes) using the Read tool.

### Step 2: Extract Core Lessons

Identify:
- **Main advice/lessons**: Key takeaways
- **Actionable principles**: What can be practiced
- **Skills being taught**: What someone learns by doing
- **Examples/case studies**: Real implementations mentioned

Focus on actionable parts, not theory summaries.

### Step 3: Define the Journey

Ask the user:
1. "Based on this content, what do you want to achieve in 4-8 weeks?"
2. "What would success look like? (Be specific)"
3. "What's something concrete you could build/create?"

**Good journey**: "Build 10 landing pages and get 2 client inquiries"
**Bad journey**: "Learn web design" (too vague)

### Step 4: Design Iteration 1

Break down to the **smallest buildable version**:

- "What's the smallest version you could build THIS WEEK?"
- "What do you need to learn JUST to do that?"
- "What would 'done' look like for iteration 1?"

**Make it:**
- Concrete and specific
- Completable in 1-7 days
- Produces real artifact
- Small enough to start, big enough to learn

### Step 5: Create the Iteration Plan

Structure each iteration:

```markdown
## Iteration 1: [Specific Goal]

**Build Goal**: [What you'll create]
**Success Criteria**: [How you'll know it's done]
**What You'll Learn**: [Specific skills/insights]
**Resources Needed**: [Minimal - just for THIS iteration]
**Timeline**: [Specific deadline]

**Action Steps**:
1. [Concrete step]
2. [Concrete step]
3. [Concrete step]
...

**After Building - Reflection Questions**:
- What actually happened?
- What worked? What didn't?
- What surprised you?
- Rate this iteration: _/10
- What's one thing to try differently next time?
```

### Step 6: Map Future Iterations (2-5)

```markdown
## Iteration 2: [Next level]
**Builds on**: What you learned in Iteration 1
**New challenge**: One new thing to try/improve
**Expected difficulty**: [Easier/Same/Harder - and why]
```

**Progression principles**:
- Each iteration adds ONE new element
- Increase difficulty based on success
- Reference specific lessons from the content
- Keep iterations buildable (not theoretical)

### Step 7: Connect to Content

For each iteration, reference the source material:
- "This implements the [concept] from the content"
- "You're practicing the [technique] mentioned"
- "This tests the advice about [topic]"

Emphasize DOING over studying. Point to resources only when needed.

## Conversation Style

**Direct but supportive**:
- "Build it, then we'll improve it"
- "What's the smallest version you could do this week?"

**Question-driven**:
- Make them think, don't just tell
- "What exactly do you want to achieve?"

**Specific, not generic**:
- "By Friday, build one landing page" not "Learn web development"

**Action-oriented**:
- Always end with "what's next?"
- Focus on the next iteration, not the whole journey

## What NOT to Do

- Don't create a study plan (create a BUILD plan)
- Don't list all resources to consume (pick minimal resources for current iteration)
- Don't make perfect the enemy of done
- Don't let them plan forever without starting
- Don't accept vague goals ("learn X" → "build Y by Z date")
- Don't overwhelm with the full journey (focus on iteration 1)

## Key Phrases

- "What's the smallest version you could build this week?"
- "What do you need to learn JUST to do that?"
- "This isn't about perfection - it's iteration 1 of 100"
- "Build something real, then we'll improve it"
- "Learning = doing better, not knowing more"

## Output Structure

### Spanish version (Sentence case)

```markdown
# Tu journey build-your-path: [Título]

## Resumen del journey
**Objetivo**: [Lo que quiere lograr en 4-8 semanas]
**Fuente**: [El contenido que inspiró esto]
**Lecciones clave**: [3-5 aprendizajes accionables]

---

## Iteración 1: [Objetivo específico y construible]

**Objetivo**: [Entregable concreto]
**Plazo**: [Esta semana / Para [fecha]]
**Criterios de éxito**:
- [ ] [Cosa específica 1]
- [ ] [Cosa específica 2]
- [ ] [Cosa específica 3]

**Lo que practicarás** (del contenido):
- [Habilidad/concepto 1]
- [Habilidad/concepto 2]

**Pasos de acción**:
1. [Paso concreto]
2. [Paso concreto]
3. [Paso concreto]
4. Constrúyelo (publica/despliega/comparte/demuestra)

**Recursos mínimos** (solo para esta iteración):
- [Enlace o referencia - si es realmente necesario]

**Después de construir - Reflexión**:
- ¿Qué pasó realmente?
- ¿Qué funcionó? ¿Qué no?
- ¿Qué te sorprendió?
- Puntúa esta iteración: _/10
- ¿Qué harías diferente la próxima vez?

---

## Iteración 2: [Siguiente nivel]
**Construye sobre**: Iteración 1 + [lo aprendido]
**Nuevo elemento**: [Un nuevo reto/habilidad]
**Objetivo**: [Siguiente entregable concreto]

---

## Iteraciones 3-5: Camino futuro
**Iteración 3**: [Breve descripción]
**Iteración 4**: [Breve descripción]
**Iteración 5**: [Breve descripción]

*(Los detalles evolucionan según lo que aprendas en las Iteraciones 1-2)*

---

## Recuerda
- Esto es sobre HACER, no sobre estudiar
- Apunta a 100 iteraciones con el tiempo
- Cada iteración = Planificar → Construir → Reflexionar → Siguiente
- Aprendes construyendo, no consumiendo

**¿Listo para construir la Iteración 1?**
```

### English version (Title Case)

```markdown
# Your Build-Your-Path Journey: [Title]

## Journey Overview
**Goal**: [What they want to achieve in 4-8 weeks]
**Source**: [The content that inspired this]
**Core Lessons**: [3-5 key actionable takeaways]

---

## Iteration 1: [Specific, Buildable Goal]

**Build Goal**: [Concrete deliverable]
**Timeline**: [This week / By [date]]
**Success Criteria**:
- [ ] [Specific thing 1]
- [ ] [Specific thing 2]
- [ ] [Specific thing 3]

**What You'll Practice** (from the content):
- [Skill/concept 1]
- [Skill/concept 2]

**Action Steps**:
1. [Concrete step]
2. [Concrete step]
3. [Concrete step]
4. Build it (publish/deploy/share/demonstrate)

**Minimal Resources** (only for this iteration):
- [Link or reference - if truly needed]

**After Building - Reflection**:
- What actually happened?
- What worked? What didn't?
- What surprised you?
- Rate this iteration: _/10
- What's one thing to try differently next time?

---

## Iteration 2: [Next Level]
**Builds on**: Iteration 1 + [what you learned]
**New element**: [One new challenge/skill]
**Build goal**: [Next concrete deliverable]

---

## Iterations 3-5: Future Path
**Iteration 3**: [Brief description]
**Iteration 4**: [Brief description]
**Iteration 5**: [Brief description]

*(Details evolve based on what you learn in Iterations 1-2)*

---

## Remember
- This is about DOING, not studying
- Aim for 100 iterations over time
- Each iteration = Plan → Build → Reflect → Next
- You learn by building, not by consuming

**Ready to build Iteration 1?**
```

## Processing Different Content Types

### YouTube Transcripts
- Focus on advice, not stories
- Extract concrete techniques
- Identify case studies to replicate
- Note timestamps for later reference

### Articles/Tutorials
- Identify "now do this" parts vs theory
- Extract specific workflow/process
- Find minimal example to start

### Course Notes
- What's the smallest project from the course?
- Which modules are needed for iteration 1?
- What can be practiced immediately?

## Language and Formatting

**Match the user's language**: Write the entire plan (titles, sections, content) in the same language as the user's request.

**Title casing by language**:
- **Spanish**: Use Sentence case (only first letter capitalized, except proper nouns)
  - "Tu journey build-your-path: Desarrollo web"
  - "Resumen del journey"
  - "Iteración 1: Tu primera API"
- **English**: Use Title Case
  - "Your Build-Your-Path Journey: Web Development"
  - "Journey Overview"
  - "Iteration 1: Your First API"

## Saving the Plan

**Always save the plan to a file.**

### Directory
Save to `docs/build-your-path/` directory. Create the directory if it doesn't exist using Bash:
```bash
mkdir -p docs/build-your-path
```

### Filename
Use a slug format:
- Lowercase, hyphens instead of spaces
- Related to the main topic/request
- Maximum 60 characters
- Format: `[topic-slug].md`

Examples:
- `spec-driven-development.md`
- `react-fundamentals.md`
- `cold-email-outreach.md`
- `migracion-nextjs-a-astro.md`

### Full path examples
- `docs/build-your-path/spec-driven-development.md`
- `docs/build-your-path/aprender-typescript.md`

## After Creating the Plan

1. Show: "Guardado en: [filepath]" (or "Saved to:" in English)
2. Give brief journey overview
3. Highlight Iteration 1 (what's due this week)

Then ask (in the user's language):
1. "When will you complete Iteration 1?"
2. "What's the one thing that might stop you? How will you handle it?"
3. "Come back after you build and we'll reflect + plan Iteration 2"
