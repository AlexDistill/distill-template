# Distill Project Template

A pre-configured project template with Claude/Cursor optimizations and the conciertoAgents subagent collection.

## What's Included

- **CLAUDE.md** — Output settings, philosophy, and agent routing triggers
- **conciertoAgents/** — 49 specialized subagents + 29 skills (as git submodule)
- **.claude/commands/** — Project-specific slash commands

## Project Structure

```
project/
├── CLAUDE.md              ← AI instructions
├── .claude/commands/      ← Slash commands
├── conciertoAgents/       ← Subagents & skills (submodule)
│
├── sources/               ← Input materials
│   ├── research/          ← Market data, competitor analysis
│   ├── assets/            ← Client logos, brand files
│   └── references/        ← Inspiration, benchmarks
│
├── notes/                 ← Working documents
│   ├── meetings/          ← Meeting notes, decisions
│   ├── briefs/            ← Project briefs, requirements
│   └── scratch/           ← Quick thoughts, brainstorms
│
├── outputs/               ← Deliverables
│   ├── drafts/            ← Work in progress
│   └── final/             ← Approved deliverables
│
├── data/                  ← Datasets, exports, CSVs
├── scripts/               ← Automation, one-off tools
└── README.md              ← Project overview
```

## How to Use This Template

### Start a new project

```bash
git clone --recursive <your-template-repo-url> new-project
cd new-project
```

> The `--recursive` flag ensures the conciertoAgents submodule is cloned too.

### Update agents in any project

```bash
cd conciertoAgents
git pull origin main
cd ..
git add conciertoAgents
git commit -m "Update agents"
```

### Available Commands

| Command | Description |
|---------|-------------|
| `/agents` | Quick reference of all available subagents |
| `/code-review` | Structured code review with security, performance, conventions |
| `/today` | List overdue and upcoming Linear tasks |

## Agent Categories

- **Design** — brand, UI, UX, creative direction, whimsy
- **Engineering** — frontend, backend, AI, DevOps, rapid prototyping
- **Marketing** — content, growth, social (TikTok, Instagram, Twitter, Reddit)
- **Product** — research, trends, value props, feedback synthesis
- **Project Management** — orchestration, sprints, shipping, experiments
- **Studio Operations** — analytics, finance, legal, support, scheduling
- **Testing** — API, performance, workflow optimization

## Philosophy

See `conciertoAgents/agents/_philosophy.md` for the core beliefs that guide all agents.

**Key principles:**
- Ship fast, iterate
- Understand real people and real behavior
- Be genuinely different, not safely similar
- Function first, then find the beauty
- Trust the process — it's chaotic but it works

