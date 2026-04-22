# cc-navigator

Know which skill, agent, or tool to reach for -- workflow navigation for Claude Code.

A [Claude Code](https://claude.ai/claude-code) skill that classifies your task and recommends the right workflow, synthesized from 11 authoritative sources including Anthropic's official skills repo, the CC creator's tips, and Anthropic engineers' guides.

## When to Use

- "How should I approach this?" -- unsure where to start
- Starting a new feature, bug fix, or refactor session
- Feeling overwhelmed by a large task and need to break it down
- Don't know which skill or agent to reach for
- Between steps -- just finished something, what's next?
- Need to find the right tool for web access, testing, or presentation

## What's Inside

- **Decision Framework** -- task classification table + workflow decision tree that routes you to the right approach
- **8 Synthesized Principles** -- cross-source best practices distilled from all 11 sources (planning, TDD, context hygiene, skills engineering, tool design, parallel execution, CLAUDE.md investment, hooks)
- **Ecosystem Quick Reference** -- web access, SWE workflow, and presentation tools at a glance
- **9 source documents** in `references/` -- full article archives and ecosystem detail guides for deep dives

## Sources

1. [Superpowers](https://github.com/obra/superpowers) -- TDD, task atomization, subagent-driven development
2. [AReaL / Starcat](https://github.com/inclusionAI/AReaL) -- 32-day zero-handwritten distributed RL
3. [CC Official: How It Works](https://code.claude.com/docs/how-claude-code-works) -- Agentic loop, context management
4. [CC Official: Hooks Guide](https://code.claude.com/docs/hooks-guide) -- 4 hook types, 19 lifecycle events
5. [Boris Cherny: CC Tips](https://x.com/bcherny/status/2017742741636321619) -- CC creator's 10 tips from the team
6. [Tw93: CC Architecture](https://x.com/HiTw93/status/2032091246588518683) -- Six-layer architecture, context governance
7. [Thariq: How We Use Skills](https://x.com/trq212/status/2033949937936085378) -- 9 skill categories, writing best practices
8. [Thariq: Seeing like an Agent](https://x.com/trq212/status/2027463795355095314) -- Tool design philosophy
9. [Harness Design](https://www.anthropic.com/engineering/harness-design-long-running-apps) -- GAN-inspired multi-agent for long tasks
10. [Anthropic Skills](https://github.com/anthropics/skills) -- Official skill spec, progressive disclosure, eval-driven skill development
11. [jiahao-shao1](https://github.com/jiahao-shao1) -- Research workflow skills, remote-cluster-agent, 5-tier web-fetcher

## Install

### Via skills.sh (recommended)

```bash
npx skills add freemty/cc-navigator
```

Works with Claude Code, Cursor, Codex, Windsurf, and [15+ other agents](https://skills.sh).

### Manual

```bash
git clone https://github.com/freemty/cc-navigator.git ~/.claude/skills/cc-navigator
```

## License

MIT
