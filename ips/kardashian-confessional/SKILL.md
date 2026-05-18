---
name: kardashian-confessional
description: FinalRound AI video IP/style library for Kardashian-family-style reality TV confessionals. Use inside finalround-ai-video when the user wants Kardashian style, reality-show confession, glam interview drama, polished-but-panicking candidate energy, creator confessionals, or hard cuts between self-presentation and real interview pressure.
---

# Kardashian Confessional

Use this as a FinalRound-specific style library, not a celebrity imitation tool.

Do not depict, name, impersonate, or reference actual Kardashian family members. Extract the reality-TV grammar: polished confessional, emotional self-narration, glamorous composure, hard-cut proof, small personal drama, and deadpan reaction.

## Core Logic

Kardashian-style reality grammar is built on a gap between self-presentation and reality.

For FinalRound, the gap is:

```
I am totally fine before the interview
→ hard cut to real interview pressure
→ composure breaks
→ FinalRound gives structure
→ character regains control but stays in confessional attitude
```

The product should enter as a practical edge during a real online interview, usually Live Interview Copilot / Desktop Stealth App. Do not turn the ad into luxury lifestyle content.

## Workflow

### Step 0: Extract the Drama

Identify:

**Self-image:** What does the candidate want people to think?

**Reality pressure:** What actually happens in the interview?

**Confessional line:** What is the first sentence that reveals denial, delusion, or panic?

**Product turn:** At what second does FinalRound help her regain structure?

### Step 1: Match a Scene Structure

Open `refs/场景结构索引表.md` and choose 2-3 candidate structures. If the user is still deciding, output candidates first.

Short direction format:

```
产品面：Live Interview Copilot / Desktop Stealth App
ICP心理：[一句话]
风格模块：Kardashian Confessional
场景结构：[索引编号 + 名称]
3秒hook：[confessional第一句话]
现实打脸：[第几秒切到真实面试压力]
FinalRound转折：[第几秒进入产品edge]
禁止项：不出现真实Kardashian人物/姓名/品牌，不出现字幕、水印、可读UI、logo、end card
```

### Step 2: Write the 15s Prompt

Use one 15-second vertical 9:16 prompt. The default structure is fixed interview-camera confessional plus hard cut to laptop interview.

Required elements:

- Fixed confessional camera, close face, polished lighting.
- One hard cut to real computer interview pressure.
- Candidate must interact with laptop/desktop in the real interview scene.
- All spoken dialogue must be English.
- No readable UI, subtitles, logo, title card, or end card.

## Visual Grammar

Use:

- close-up confessional framing
- soft bright reality-show lighting
- clean makeup/hair/outfit
- composed posture breaking for one second
- hard cuts, reaction shots, slight eye-rolls, deadpan pauses
- elegant bedroom, closet, vanity, kitchen island, or clean home-office setup

Avoid:

- actual Kardashian names, likenesses, show titles, logos, or catchphrases
- luxury flex as the main idea
- handheld chaos unless it is the reality cutaway
- dark cinematic lighting
- long monologues that cannot fit into 15 seconds

## Dialogue Rules

The first line should sound like a confession, not an ad.

Good shapes:

- "I said I was calm. That was inaccurate."
- "I love pretending I'm prepared."
- "I was giving confident. My brain was giving nothing."
- "I thought the interview was going to be cute. It was not."

Keep the product line short:

- "Open FinalRound AI."
- "I need structure."
- "Not a pep talk. Structure."

## QA

Before finalizing:

- Is it a reality-confessional structure, not generic influencer talking head?
- Does the reality cut prove the confession?
- Is the product turn tied to real interview pressure?
- Did it avoid actual Kardashian people, names, show titles, and likenesses?
- Did it keep all spoken dialogue English?
- Did it avoid readable UI, logo, subtitles, watermarks, and end card?
