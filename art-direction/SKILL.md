---
name: art-direction
description: Apply art direction principles to image generation prompts. Use when generating, editing, or reviewing prompts for AI image generation. Triggers on image generation requests, prompt writing, visual direction, art direction, promptcraft, and any request to create or refine an image prompt.
---

# Art Direction Skill

Apply the Promptcraft framework when writing or reviewing image generation prompts. Constraints produce quality; vague prompts produce default aesthetics.

## Before Writing Any Prompt

Read the Prompt Stack. Follow it in order. Never skip layers.

## The Prompt Stack (influence order)

1. **Subject & purpose** — what is the image for
2. **Context & story** — where, when, why
3. **Composition** — framing, camera position, focal point
4. **Light** — source, direction, softness, time of day
5. **Materials & realism cues** — surface, wear, physics
6. **Color & palette** — controlled, intentional
7. **Style** — only if needed, and scoped
8. **Quality & output parameters** — aspect ratio, seed
9. **Negative prompt** — what must not appear

## Rules

- **One primary idea, three supporting constraints.** Do not stack styles or contradictory cues.
- **Always include a negative prompt.** Exclude tonal, texture, and color violations — not just "no text" but "no muddy tones, no cheap neon, no rainbow oversaturation."
- **Default palette: controlled neutrals + one accent.** Declare dominant, secondary, accent. Constrain saturation intentionally.
- **Camera controls are mandatory.** Specify lens, perspective, depth of field. Do not skip them.
- **Light controls are mandatory.** Specify time of day, source type, contrast. Do not skip them.
- **Never write a subject-only prompt.** A subject without constraints yields default aesthetics.
- **Use AI as prompt editor, not author.** Generate variations from constraints, then curate and lock.

## Camera Quick Reference

- 24mm — drama, wide distortion
- 35mm — natural, environmental
- 50mm — intimate, balanced
- 85mm — portrait compression, shallow DOF

## Light Quick Reference

- Morning — long soft shadows, warm
- Golden hour — directional, warm, high contrast
- Overcast — even, soft, low contrast
- Dusk — cool, muted, atmospheric

## Negative Prompt Defaults

When no specific exclusions are given, include:

> No cluttered backgrounds, muddy tones, flat contrast, harsh shadows, cheap neon, rainbow oversaturation, cartoon styling, blurry focus, watermarks, text overlays, generic AI artifacts

## Specificity Rule

- **Good specificity:** era, materials, camera position, light direction, lens choice
- **Bad specificity:** hex colors for every element, contradictory style mashups, over-specified placement instructions that the model will ignore

When in doubt, constrain the 3-4 decisions that matter most and let the model handle the rest.

## Iteration Strategy

1. Start with the full Prompt Stack
2. Refine based on output — adjust 1-2 layers at a time
3. If the output is fundamentally wrong, start over with a different primary idea
4. Do not pile constraints onto a failing prompt — fewer, sharper constraints beat more, muddier ones

## When to Use This Skill

- Any image generation request
- Reviewing or improving an existing prompt
- Providing art direction feedback on generated images
- Creating visual direction documentation