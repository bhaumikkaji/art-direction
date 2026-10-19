# AGENTS.md

Instructions for an AI agent installing or using this skill for a user.

## Install

The skill is the `art-direction/` folder (a `SKILL.md` plus `references/`). Copy that folder, not the whole repo, into your skills directory:

```bash
git clone https://github.com/bhaumikkaji/art-direction.git /tmp/art-direction
```

- Claude Code: `cp -R /tmp/art-direction/art-direction ~/.claude/skills/`
- OpenClaw: `cp -R /tmp/art-direction/art-direction ~/.openclaw/workspace/skills/`, then reload skills
- Other agents: copy it into the folder your agent loads skills from. If it has none, read `art-direction/SKILL.md` before writing any image prompt and follow it.

Check `SKILL.md` sits directly inside the copied `art-direction/` folder, then tell the user it's ready.

## Use

Load `art-direction/SKILL.md` whenever the user asks you to write, refine or review an image generation prompt. Follow the Prompt Stack in order, always set camera and light, and always include a negative prompt. Use `references/style-catalog.md` only alongside those constraints, never instead of them.
