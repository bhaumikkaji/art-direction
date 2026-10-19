# art-direction

An agent skill that applies art direction principles to image generation prompts. Works with Claude Code, OpenClaw and any agent that reads `SKILL.md` files.

Based on the **Promptcraft framework** from Alberto Cerriteno's talk, [Promptcraft: Art Direction for Generative Imagery](https://www.youtube.com/watch?v=prKWjCqO4dk).

## What it does

When any agent generates, edits, or reviews an image prompt, this skill enforces:

- **The Prompt Stack** — ordered constraints: subject → context → composition → light → materials → color → style → quality → negative
- **Camera controls** — lens choice, depth of field, perspective, motion
- **Light controls** — time of day, source, contrast, mood
- **Default palette rule** — controlled neutrals + one accent
- **Negative prompts** — aesthetic boundaries, not just "no text"
- **Specificity rule** — one primary idea, three supporting constraints

## Install

The skill lives in the `art-direction/` folder. Copy that folder into your agent's skills directory.

**Claude Code**

```bash
git clone https://github.com/bhaumikkaji/art-direction.git /tmp/art-direction
cp -R /tmp/art-direction/art-direction ~/.claude/skills/
```

**OpenClaw**

```bash
openclaw skills install https://github.com/bhaumikkaji/art-direction
```

Or copy it by hand:

```bash
git clone https://github.com/bhaumikkaji/art-direction.git /tmp/art-direction
cp -R /tmp/art-direction/art-direction ~/.openclaw/workspace/skills/
```

**Any other agent:** copy `art-direction/` into the folder your agent loads skills from, or point it at `AGENTS.md`.

## Use it

Once installed, it kicks in whenever you ask your agent to write, improve or review an image prompt. For example:

> Write a prompt for a hero image of a ceramic coffee cup on a kitchen counter for a product page.

The agent builds the prompt layer by layer (subject, context, composition, light, materials, color, style, output settings, negative prompt) and picks a lens and light setup instead of leaving them to the model.

## Skill structure

```
AGENTS.md                 # Install steps for agents
art-direction/
├── SKILL.md              # Core framework and rules
└── references/
    └── style-catalog.md  # Style labels with usage caveats
```

## Origin

Distilled from Alberto Cerriteno's talk [Promptcraft: Art Direction for Generative Imagery](https://www.youtube.com/watch?v=prKWjCqO4dk). Watch it for the full reasoning and examples.

## License

MIT for the skill text in this repo. The Promptcraft framework itself is Alberto Cerriteno's work; credit him if you build on it.