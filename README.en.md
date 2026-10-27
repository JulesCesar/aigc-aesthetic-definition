# AIGC Aesthetic Definition Skill

> **Turn an image idea into executable aesthetic parameters — then write the prompt.**
> [中文](README.md)

A skill pack for AI coding assistants that support skill directories that decomposes a shot into *light → material → style → lens* before writing the prompt, so it avoids adjective stacking and the "AI look".

## What it fixes

- **Flat image**: "cinematic" with no light position, ratio or color temperature
- **Plastic / CG look**: materials described with adjectives only, no reflection model or defects
- **Style drift**: illustration / game / art-movement tokens turn photorealism into a painting
- **Character inconsistency**: no reference image, no consistency anchors
- **Wrong counts**: nine tails drawn as one, three tentacles drawn as five

## Install

```bash
git clone https://github.com/JulesCesar/aigc-aesthetic-definition.git \
  ~/.agents/skills/aigc-aesthetic-definition
```

Or copy the folder into `~/.agents/skills/` (some tools also read `~/.claude/skills/`).

## Contents

```
SKILL.md                    when to use, three elements, prompt skeleton, four rules, quick diagnosis
references/light.md         light in four dimensions: source/quality/position/color + emotion map + "where light lands"
references/material.md      how to write materials + eight material directions
references/styles.md        which styles are safe, which destroy photorealism
references/formula.md       six lighting modules + lens/film + video prompt pattern
references/anti-patterns.md do-not-use list + 15 failure modes + 9-point checklist
```

## Usage

Just ask in natural language:

- "Write a night-scene prompt for my fox character."
- "This image looks flat — diagnose it with the aesthetic framework."
- "Should I add this style token?"

The assistant loads the skill and returns a copy-ready block following *subject → light → material → lens → quality → negative*.

## One core rule

> **Write physics, not adjectives.**

Not "premium feel", but "single 45° soft key, 5600K, 1:3 ratio, light landing on the nose bridge and cheekbone".

## Scope

This repository contains method, judgement rules and generic templates only. It contains **no screenplay, character bible, scene description from any specific project, and no book content**.

## Attribution

The framework draws on publicly available material about AIGC prompting and photographic aesthetics, rewritten from the author's own practice.

This skill is an **independent digest**: it quotes no book text or sample images, and is not authorized by any publisher.

## License

MIT
