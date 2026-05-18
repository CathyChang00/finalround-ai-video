---
name: finalround-ai-video
description: "FinalRound AI video skill for generating or reviewing FinalRound / FinalRound AI / FRAI social ads, interview copilot videos, Live Interview Copilot scripts, 9:16 Instagram Reels / TikTok / INS prompts, UGC creator briefs, trend-to-FinalRound adaptations, FinalRound video QA, and style modules such as MrBeast Challenge, Kardashian Confessional, and AI Fruit Short Drama. Must follow this skill's canonical FinalRound-INS rules and samples: references/finalround-ins.md and references/finalround-ins-samples.md."
---

# FinalRound AI Video

Use this as the top-level FinalRound video production skill.

Do not invent a separate FinalRound creative system. The canonical rules are:

1. `references/finalround-ins.md`
2. `references/finalround-ins-samples.md`

Always load `references/finalround-ins.md` before creating, rewriting, or judging any FinalRound video concept, prompt, script, creator brief, or ad direction.

Load `references/finalround-ins-samples.md` when the user asks for a finished prompt, asks for examples, references a previous FinalRound style, or when the output needs calibration against battle-tested samples.

Load style/IP libraries when the user requests a style tilt. These libraries are pure style research libraries, not FinalRound-specific templates:

1. `ips/kardashian-confessional/SKILL.md` for Kardashian-style reality confessional grammar.
2. `ips/ai-fruit-short-drama/SKILL.md` for AI fruit short drama / Fruit Love Island grammar.
3. MrBeast-style challenge grammar only when explicitly requested.

## Source Relationship

These two reference files are the source of truth inside this skill:

- `references/finalround-ins.md`
- `references/finalround-ins-samples.md`

Do not defer FinalRound prompt structure to another video skill. External style libraries can provide camera grammar or genre flavor, but FinalRound product framing, dialogue rules, CTA behavior, and QA rules come from this skill.

## Default Execution

1. Read `references/finalround-ins.md`.
2. Classify the request using its workflow: product face, ICP psychology, style module, comedy mode, visual template, hook, turn, restrictions.
3. If the style module is Kardashian Confessional or AI Fruit Short Drama, read the matching `ips/` library and its style index before proposing concepts. Extract style elements first; do not force the library into a FinalRound-specific template.
4. If writing a prompt, also read `references/finalround-ins-samples.md` and match its level of specificity.
5. Output in the format requested by the user. If the user is still discussing direction, use the short direction format from `finalround-ins.md`; if the user asks for a prompt, write the full 15-second 9:16 prompt.
6. Run the QA rules in `finalround-ins.md` before finalizing.

## Hard Rules

- Do not add new content buckets, style modules, comedy modes, visual templates, product claims, or prompt rules unless the user explicitly asks to evolve the skill.
- Do not replace the source files with a summarized version.
- Do not turn FinalRound into generic AI-video, generic SaaS, or generic career advice.
- Do not confuse Live Interview Copilot / Desktop Stealth App with Mock Interview.
- Do not add readable UI, logo, captions, subtitles, title cards, end cards, or Chinese spoken dialogue unless the source rules or user explicitly override it.
