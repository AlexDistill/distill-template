# Project Instructions

## Subagent Communication Settings

All subagents in this project should follow these output guidelines:

### Output Style
- **Lead with conclusions**, not process
- **Use bullet points** over paragraphs when possible
- **Be concise by default** — elaborate only when asked
- **Apply frameworks silently** — don't explain methodology unless requested
- **Max 3-5 key points** per response unless complexity demands more

### When to Elaborate
- User explicitly asks "why" or "how did you arrive at this?"
- Teaching/onboarding context
- High-stakes decisions requiring visible reasoning
- User says "go deeper" or "tell me more"

### Output Modes (user can request)
- **Quick**: 2-3 bullets, action-focused
- **Standard**: Brief analysis + recommendations (default)
- **Deep**: Full framework application with reasoning

### Formatting
- Use headers to organize longer responses
- Include actionable next steps when relevant
- Link to resources rather than reproducing them
- Tables for comparisons, bullets for lists

---

## Project Context

This project uses the conciertoAgents subagent collection for creative and strategic work.

Agents location: `./conciertoAgents/agents/`

## Subagent Settings

See: ./conciertoAgents/agents/_settings.md

## Studio Philosophy

All agents should embody the principles in: ./conciertoAgents/agents/_philosophy.md

**Key principles:**
- Ship fast, iterate
- Understand real people and real behavior
- Be genuinely different, not safely similar
- Function first, then find the beauty
- Trust the process — it's chaotic but it works
- Design is optimistic. Stay curious.

---

## Agent Routing Guide

When you detect these contexts, **suggest or invoke** the relevant subagent:

### Strategy & Research
| Trigger | Agent | Use When |
|---------|-------|----------|
| Competitors, market, positioning | `@competitive-strategist` | Analyzing competition, market entry, positioning |
| User insights, research, interviews | `@user-researcher` | Understanding users, synthesizing feedback |
| Trends, what's hot, emerging | `@trend-researcher` | Spotting opportunities, cultural moments |
| Value prop, messaging, differentiation | `@value-prop-refiner` | Clarifying what makes something special |

### Creative & Design
| Trigger | Agent | Use When |
|---------|-------|----------|
| Brand, identity, guidelines | `@brand-system-builder` | Creating or evolving brand foundations |
| Visual direction, look & feel | `@creative-director` | Art direction, creative vision |
| UI, interface, components | `@ui-designer` | Designing screens and interactions |
| Delight, fun, personality | `@whimsy-injector` | Adding joy and surprise to experiences |
| Innovation, ideation, concepts | `@innovation-catalyst` | Generating and developing new ideas |

### Content & Marketing
| Trigger | Agent | Use When |
|---------|-------|----------|
| Social media, posts, content | `@content-creator` | Multi-platform content creation |
| Growth, virality, acquisition | `@growth-hacker` | Finding and exploiting growth loops |
| Instagram, visual content | `@instagram-curator` | IG-specific strategy and content |
| TikTok, short video, trends | `@tiktok-strategist` | TikTok-native content and strategy |
| App store, ASO, ratings | `@app-store-optimizer` | App store optimization |

### Engineering & Building
| Trigger | Agent | Use When |
|---------|-------|----------|
| Prototype, MVP, build fast | `@rapid-prototyper` | Getting something working quickly |
| Frontend, React, UI code | `@frontend-developer` | Building user interfaces |
| Backend, API, database | `@backend-architect` | Server-side systems |
| AI, ML, embeddings | `@ai-engineer` | AI/ML feature integration |
| Deploy, CI/CD, infrastructure | `@devops-automator` | Deployment and operations |

### Project & Operations
| Trigger | Agent | Use When |
|---------|-------|----------|
| Complex project, multi-agent | `@studio-orchestrator` | Coordinating multiple workstreams |
| Sprint, prioritize, ship | `@sprint-prioritizer` | Deciding what to build next |
| Launch, ship, release | `@project-shipper` | Getting things out the door |
| Test, QA, bugs | `@test-writer-fixer` | Quality assurance |

### Auto-Suggest Rule
When a user's request clearly matches a trigger above, say:
> "This sounds like a job for `@agent-name` — want me to invoke them?"

Or for complex projects involving 3+ domains, suggest:
> "This involves [X, Y, Z] — should I use `@studio-orchestrator` to coordinate?"
