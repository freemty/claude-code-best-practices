# claude-code-best-practices

Your Claude Code workflow advisor -- recommends the right skill, agent, or workflow for any task based on 9 curated best practice sources.

## Install

**Option 1: Manual (recommended)**

```bash
mkdir -p ~/.claude/skills/claude-code-best-practices
curl -sL https://raw.githubusercontent.com/freemty/claude-code-best-practices/main/skills/claude-code-best-practices/SKILL.md \
  -o ~/.claude/skills/claude-code-best-practices/SKILL.md
```

**Option 2: Git clone**

```bash
git clone https://github.com/freemty/claude-code-best-practices.git ~/.claude/plugins/claude-code-best-practices
```

Then add to your `~/.claude/settings.json`:
```json
{
  "plugins": ["~/.claude/plugins/claude-code-best-practices"]
}
```

## What it does

- **Classifies your task** (feature, bug, refactor, debug, review, planning...) based on signal keywords
- **Recommends the optimal workflow** -- which skill to invoke, in what order (TDD, parallel agents, worktrees, etc.)
- **Provides a knowledge base** of synthesized best practices from 9 authoritative sources

## When it triggers

- "How should I approach this?"
- Starting a new task, feature, or debug session
- Unsure which skill or agent to use next

## What's inside

| Section | Content |
|---------|---------|
| Decision Framework | Task classification table + workflow decision tree |
| Skills Quick Reference | Universal skills with one-line "when to use" descriptions |
| Knowledge Base | 9 curated sources with key takeaways |
| Synthesized Principles | 8 cross-source principles for daily practice |

## Sources

This skill synthesizes best practices from:

1. [Superpowers Framework](https://github.com/obra/superpowers) -- TDD, task atomization, subagent-driven development
2. [AReaL / Starcat](https://github.com/inclusionAI/AReaL) -- 32-day zero-handwritten distributed RL, layered config architecture
3. [Everything Claude Code](https://github.com/affaan-m/everything-claude-code) -- 25 agents + 108 skills closed-loop system
4. [Claude Code Official: How It Works](https://code.claude.com/docs/how-claude-code-works) -- Agentic loop, context management
5. [Claude Code Official: Hooks Guide](https://code.claude.com/docs/hooks-guide) -- 4 hook types, 19 lifecycle events
6. [Anthropic: Effective Context Engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) -- Minimal high-signal token set
7. [Anthropic: Demystifying Evals](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) -- Eval infrastructure for agents
8. [Manus: Context Engineering](https://manus.im/blog/Context-Engineering-for-AI-Agents-Lessons-from-Building-Manus) -- KV cache, append-only context
9. Community resources -- [skills.sh](https://skills.sh/), [OpenClaw Setup](https://github.com/jiahao-shao1/openclaw-setup)

## Example

> **You:** "I need to add OAuth to my app, how should I approach this?"
>
> **Claude** (with skill loaded): Classifies as "New feature" + "Planning needed". Recommends:
> 1. `superpowers:brainstorming` to explore requirements
> 2. `superpowers:writing-plans` to create implementation plan
> 3. `superpowers:test-driven-development` to implement with tests first

## License

MIT
