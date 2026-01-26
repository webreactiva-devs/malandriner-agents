# Advanced Prompt Patterns for Code

## Structure of a Good Prompt

```
[CONTEXT] - What technologies, where in the project
[OBJECTIVE] - What you want to achieve (outcome, not steps)
[CONSTRAINTS] - Limitations, conventions, what NOT to do
[FORMAT] - How you want the response
```

## Core Strategies

### Strategy 1: Context-First Prompting

Always provide sufficient context before making requests.

**Poor Approach:**
```
Create a user profile feature.
```

**Better Approach:**
```
I'm working on a web application for a fitness tracking platform.
We need to add user profile functionality.

Context:
- Technology: React frontend, Node.js backend
- User base: Health-conscious individuals, age 18-65
- Key constraint: Must comply with GDPR for EU users
- Integration: Will connect with existing authentication system

Please help me create the user profile feature.
```

### Strategy 2: Phased Interaction

Work through phases sequentially. Complete each phase before moving to the next.

**Phase 1 - Requirements:**
```
Let's start with requirements for [feature name].

Current situation: [describe current state]
Problem to solve: [describe the problem]
Success criteria: [how we'll know it works]

Help me develop clear requirements.
```

**Phase 2 - Design (after requirements approved):**
```
Now that we have clear requirements, let's create the technical design.

Requirements summary: [key requirements]
Technical context: [architecture, frameworks]
Constraints: [performance, scalability, security]

Propose a technical design.
```

**Phase 3 - Implementation (after design approved):**
```
With the design finalized, let's implement.

Design summary: [key components]
Start with: [first component to build]

Let's build this incrementally.
```

### Strategy 3: Iterative Refinement

Treat development as conversation, not single requests.

**Initial Request:**
```
Help me define requirements for email notifications.
```

**Refinement Round 1:**
```
Great start! Let's refine:
1. Can we add daily digest option?
2. How should we handle pending notifications when preferences change?
3. Elaborate on GDPR compliance for unsubscribe.
```

**Refinement Round 2:**
```
Now let's add:
- Mobile push notifications
- Notification history (last 30 days)
- Per-type controls (not just global on/off)
```

### Strategy 4: Example-Driven Prompting

Provide concrete examples of what you want.

```
I need acceptance criteria for a file upload feature.

Good example from our auth feature:
"WHEN a user enters valid credentials THEN authenticate within 2 seconds"

Avoid vague criteria like:
"System should handle file uploads efficiently"

Focus on specific, testable criteria for:
- File size limits
- Supported file types
- Upload progress indication
- Error handling
```

### Strategy 5: Constraint-Explicit Prompting

Make all constraints explicit. Don't assume AI knows your limitations.

```
Design a caching strategy for product catalog.

Explicit constraints:
- Infrastructure: AWS with Redis, PostgreSQL
- Performance: API response < 200ms for cached data
- Scale: 10,000 products, 1,000 concurrent users
- Freshness: Updates visible within 5 minutes

Flexibility allowed:
- Cache invalidation strategy
- Cache key structure
- Failover approach
```

### Strategy 6: Role-Based Prompting

Frame requests from specific perspectives.

**As a junior learning:**
```
Explain this code as if I'm a junior with 6 months experience.
- What does each part do?
- Why these choices instead of alternatives?
- What would break if I changed X?
```

**As a senior reviewing:**
```
Review this code as a strict senior engineer.
- Security vulnerabilities
- Performance issues
- Maintainability concerns
- Missing edge cases
```

### Strategy 7: Validation-Oriented Prompting

Build quality checks into your prompts.

```
Review this code and check:
1. Are all inputs validated?
2. Are error cases handled?
3. Are there any security concerns?
4. What edge cases might fail?
5. Does it follow project conventions?

Provide specific issues with line references.
```

### Strategy 8: Trade-Off Exploration

Explore options rather than seeking single answers.

```
We need real-time notifications. Compare:

Option A: WebSocket connections
Option B: Server-Sent Events (SSE)
Option C: Long polling

For each, evaluate:
- Implementation complexity
- Browser compatibility
- Server resource usage
- Scalability

Present trade-offs in a comparison table.
```

## Patterns by Situation

### The Explorer (for unknown code)

```
I just joined a project with [stack].
Looking at file [name].

Questions:
1. What's the main purpose of this file?
2. What are the key functions and what do they do?
3. How does it connect to other files?
4. What patterns or conventions does it follow?
```

### The Structured Debugger

```
Problem: [brief description]

Expected behavior:
[what should happen]

Actual behavior:
[what happens instead]

Relevant code:
[paste only what's needed]

What I already tried:
[list attempts]

Stack trace (if applicable):
[paste complete error]
```

### The Safe Refactorer

```
I want to refactor this code:
[current code]

Refactoring goals:
- [goal 1: e.g., separate responsibilities]
- [goal 2: e.g., improve testability]

Constraints:
- Keep public API the same
- Don't change behavior
- [other constraints]

Give me refactored code and explain each change.
```

### The Active Learner

```
I think this code does [what you believe].

Specific questions:
1. On line X, why use [thing] instead of [alternative]?
2. What would happen if [edge case]?
3. Does this pattern have a name? Where can I learn more?

[paste code]
```

### The Iterative Builder

```
Let's build [feature] step by step.

Start with the simplest working version.
Then we'll add:
1. [improvement 1]
2. [improvement 2]
3. [improvement 3]

For each step, show code and explain
what we added and why.

Project context:
[technologies and structure]
```

## Emergency Prompts

### "Nothing Works and I'm Frustrated"
```
Stuck for [time] with [problem].

Already tried:
- [thing 1]
- [thing 2]

Using: [exact versions]

Give me a step-by-step diagnostic checklist
to find the root cause.
```

### "I Need to Deliver Soon"
```
I need [functionality] working in [time].

Minimum viable version:
[what's absolutely necessary]

Nice to have (if time):
[optional improvements]

Give me the simplest, fastest solution that works,
even if it's not the most elegant.
```

### "I Don't Understand the Error"
```
I get this error but don't understand it:

[complete error, not truncated]

Explain:
1. What this error means in simple terms
2. Most common causes
3. How to diagnose which is my case
```

## Anti-Patterns (What NOT to Do)

### Vague Prompt
```
BAD: "Make it work better"
GOOD: "Reduce response time from 3 seconds to under 500ms"
```

### No Context
```
BAD: "Why does it error?"
GOOD: "Running `npm run build` in Next.js 14,
      I get this error: [complete error]"
```

### Too Long
```
BAD: [50 lines of code + project history]
GOOD: [only relevant code + minimum context]
```

### Multiple Unrelated Questions
```
BAD: "Fix the bug, add tests, and explain Docker"
GOOD: One prompt per topic, in priority order
```

## Common Mistakes

1. **Too little context:** AI can't read your mind
2. **All at once:** Work in phases, not giant prompts
3. **Accept first response:** Iterate and refine
4. **No examples:** Show what you want
5. **Hidden constraints:** Make limitations explicit
6. **Skip validation:** Always verify outputs
