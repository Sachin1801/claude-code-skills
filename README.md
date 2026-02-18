# Claude Code Skills

Custom [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills I use for day-to-day development. Each skill is a Markdown file that gives Claude Code domain-specific knowledge and workflows.

## Skills

| Skill | Description | Install |
|-------|-------------|---------|
| [UI/UX Pro Max](skills/ui-ux-pro-max/ui-ux-pro-max.md) | Design intelligence — 50+ styles, 97 color palettes, 57 font pairings, 99 UX guidelines across 9 tech stacks | Project-level |
| [Mintlify](skills/mintlify/mintlify.md) | Build and maintain documentation sites with Mintlify — CLI commands, page structure, components, API docs | Global |
| [Vercel Web Guidelines](skills/vercel/vercel-starter.md) | Review UI code for Vercel Web Interface Guidelines — accessibility, focus states, forms, animation, performance | Global |

## How to Use

### Project-level skill (lives in the project repo)

Copy the `.md` file into your project's `.claude/skills/` directory:

```bash
mkdir -p .claude/skills
curl -o .claude/skills/ui-ux-pro-max.md \
  https://raw.githubusercontent.com/Sachin1801/claude-code-skills/main/skills/ui-ux-pro-max/ui-ux-pro-max.md
```

### Global skill (available across all projects)

Copy into your user-level Claude config:

```bash
mkdir -p ~/.claude/skills
curl -o ~/.claude/skills/mintlify.md \
  https://raw.githubusercontent.com/Sachin1801/claude-code-skills/main/skills/mintlify/mintlify.md
```

## What Are Claude Code Skills?

Skills are Markdown files (`.md`) placed in `.claude/skills/` that teach Claude Code domain-specific knowledge. They're loaded into context when Claude detects a matching task based on the skill's `description` field in the frontmatter.

- **Project-level:** `.claude/skills/` in your repo — shared with the team via git
- **Global:** `~/.claude/skills/` — available across all your projects

Each skill has YAML frontmatter with a `name` and `description` that Claude uses to decide when to apply the skill.

## License

MIT
