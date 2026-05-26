---
name: finalround-ai-video
description: "FinalRound AI video skill for generating or reviewing FinalRound / FinalRound AI / FRAI social ads, interview copilot videos, Live Interview Copilot scripts, 9:16 Instagram Reels / TikTok / INS prompts, UGC creator briefs, trend-to-FinalRound adaptations, FinalRound video QA, R2 character asset references, and style / IP adaptation modules such as MrBeast Challenge, Kardashian Confessional, AI Fruit Short Drama, Matrix-like control systems, 1984-like recruiting screens, Squid Game-like interview elimination, and other safe genre translations. Must follow this skill's canonical FinalRound-INS rules, samples, R2 asset workflow, and IP adaptation rules: references/finalround-ins.md, references/finalround-ins-samples.md, references/r2-character-assets.md, and references/ip-adaptation.md."
---

# FinalRound AI Video

Use this as the top-level FinalRound video production skill.

Do not invent a separate FinalRound creative system. The canonical rules are:

1. `references/finalround-ins.md`
2. `references/finalround-ins-samples.md`
3. `references/r2-character-assets.md` when the user mentions R2 assets, named character assets, reference identities, or asks to generate with stored characters.
4. `references/ip-adaptation.md` when the user references a film, TV show, game, historical ceremony, genre scene, or says a video should feel like a known IP.

Always load `references/finalround-ins.md` before creating, rewriting, or judging any FinalRound video concept, prompt, script, creator brief, or ad direction.

Load `references/finalround-ins-samples.md` when the user asks for a finished prompt, asks for examples, references a previous FinalRound style, or when the output needs calibration against battle-tested samples. Treat all numbered sample entries as one canonical sample list; do not create separate sample tiers. If Cathy marks a sample as unfinished or draft, exclude it from durable rule extraction until she approves it.

Load `references/r2-character-assets.md` when Cathy says the character exists in R2, names an R2 asset role, names a known stored character such as Dario / Karpathy / Zuckerberg / Peter Thiel / Truman / Jessica, or asks to generate video using stored assets. Asset references must be resolved at the API layer, not recreated only through prompt text.

Load `references/ip-adaptation.md` when Cathy asks for an IP/movie/game/ceremony feeling such as Matrix, 1984, Squid Game, Oppenheimer, Godfather, Napoleon coronation, Blade Runner, LOTR, MrBeast, or any "像某个经典场面" direction. Use it to translate the source into safe FinalRound genre grammar; do not put original IP names, character names, actors, logos, quotes, or recognizable copyrighted dialogue into generation prompts.

Load style/IP libraries when the user requests a style tilt. These libraries are pure style research libraries, not FinalRound-specific templates:

1. `ips/kardashian-confessional/SKILL.md` for Kardashian-style reality confessional grammar.
2. `ips/ai-fruit-short-drama/SKILL.md` for AI fruit short drama / Fruit Love Island grammar.
3. MrBeast-style challenge grammar only when explicitly requested.

## Source Relationship

These reference files are the source of truth inside this skill:

- `references/finalround-ins.md`
- `references/finalround-ins-samples.md`
- `references/r2-character-assets.md`
- `references/ip-adaptation.md`

Do not defer FinalRound prompt structure to another video skill. External style libraries can provide camera grammar or genre flavor, but FinalRound product framing, dialogue rules, CTA behavior, and QA rules come from this skill.

## Default Execution

1. Read `references/finalround-ins.md`.
2. Classify the request using its workflow: product face, ICP psychology, social/status dynamic, camera ownership, spatial blocking, reveal mechanism, close-up density, audio/BGM handling, style module, comedy mode, visual template, hook, turn, restrictions.
3. For INS / Instagram / TikTok work, establish a one-line English POV before writing or optimizing the full prompt, unless the user already gives a locked POV. Treat the POV as the video's north star: it should state the viewer-facing situation, not the product explanation.
4. If the user asks to optimize the skill from approved prompts, patch durable rules in `references/finalround-ins.md`; do not only add examples. Base the rules on finished prompts, and skip any prompt Cathy calls unfinished.
5. If the user is iterating from generated videos, preserve the variables they liked, use reference videos when supported, and vary only one main variable per new version.
6. If the style module is Kardashian Confessional or AI Fruit Short Drama, read the matching `ips/` library and its style index before proposing concepts. Extract style elements first; do not force the library into a FinalRound-specific template.
7. If writing a prompt, also read `references/finalround-ins-samples.md` and match its level of specificity.
8. If the prompt uses a stored character or real-person-style reference, resolve the R2 asset first. Use `references/r2-character-assets.md` to find the `chars/` asset slug, re-check the exact image key with `rclone lsf`, presign it through the creative API storage layer, and pass the URL as `image_url`, `image_urls`, or `reference_images` according to the provider. In the generation prompt, refer to it only as `Reference [1]`, `Reference [2]`, etc.
9. If the prompt borrows IP or genre grammar, load `references/ip-adaptation.md`, convert the source into a safe template label, and decide whether the idea is already connected to FinalRound or still `未接产品 / 待转化`.
10. Output in the format requested by the user. If the user is still discussing direction, use the short direction format from `finalround-ins.md`; if the user asks for a prompt, write the full 15-second 9:16 prompt.
11. Run the QA rules in `finalround-ins.md` before finalizing.

## Hard Rules

- Do not add new content buckets, style modules, comedy modes, visual templates, product claims, or prompt rules unless the user explicitly asks to evolve the skill.
- Do not replace the source files with a summarized version.
- Do not turn FinalRound into generic AI-video, generic SaaS, or generic career advice.
- Do not confuse Live Interview Copilot / Desktop Stealth App with Mock Interview.
- Do not add readable UI, logo, captions, subtitles, title cards, end cards, or Chinese spoken dialogue unless the source rules or user explicitly override it.
- Do not put platform-risky real-person identity terms or intermediate labels into the generation prompt when an R2 asset can carry that identity. Use the actual reference image and direct wording such as `Use Reference [1] as the exact character identity`.
- Do not paste R2 paths into prompts as if the model can fetch them. R2 paths are for the agent/API layer; prompts should use `Reference [n]`.
- Do not copy an IP library wholesale into FinalRound prompts. Translate IPs into original genre grammar and product-relevant job interview structures.
