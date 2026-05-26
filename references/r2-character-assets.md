# R2 Character Assets

Source checked: `r2:creative-assets/chars/`

Last checked: 2026-05-26

Use this file as a lightweight `chars/` asset slug index, not as a file-level image path list. Before generating with an R2 character, re-check the exact image key with:

```text
rclone lsf r2:creative-assets/chars/<asset-slug> --recursive
```

## Asset-First Rule

When Cathy says a character exists in R2, resolve the R2 asset and pass it as an actual image reference to the generation provider. Do not rely on prompt text to recreate a real person, company figure, or platform-sensitive identity.

In the prompt, refer to the image as `Reference [1]`, `Reference [2]`, etc. Do not add intermediate identity labels just to explain who the asset resembles. The reference image carries the identity; the prompt should describe only the role in the current scene, action, posture, and emotion.

Do not paste R2 paths into the generation prompt as if the model could fetch them. R2 paths are for the agent/API layer; the prompt should only say `Reference [1]`.

## Current Chars Index

```text
ace-attorney-court
ace-attorney-elon
ace-attorney-sam
alexandr-wang
andrej-karpathy
anthropic-cofounders
captain-america
cursor-ceo
dario-amodei
dario-papal
demis-hassabis
elon-musk
garry-tan
hou-liangping
jack-nicholson
jeff-bezos
jensen-huang
jing-yang
lee-jung-jae
liu-yuan
lucy-liu
mark-zuckerberg
meryl-burbank
mira-murati
modi
morgan-freeman
pete-hegseth
peter-thiel
pope-leo-xiv
robin-li
sam-altman
sheldon-cooper
squid-game-meta-doll
steve-carell
sundar-pichai
truman
trump
xiao-hong
yann-lecun
```

## Default Casting Aliases

Use these as FinalRound social skit defaults when Cathy uses shorthand. Resolve the slug as a real R2 image reference first; in the generation prompt, refer to it only as `Reference [n]`.

| Shorthand | Default R2 slug | Default role |
|---|---|---|
| 亚男 / Asian male student / Asian male nerd | `jing-yang` | high-pressure Asian male candidate, nervous but high-achieving |
| 亚女面试官 / Asian female interviewer | `lucy-liu` | calm, sharp interviewer or hiring manager |
| 白男 nerd / white male nerd | `sheldon-cooper` | rigid, overprepared, socially awkward technical candidate |
| 白男肌肉男 / athletic white male / jock | `captain-america` | confident athletic white male candidate or winner archetype |
| 闪灵 / 崩溃的打工人 | `jack-nicholson` | burned-out worker on the edge of a meltdown |
| Michael / Micheal / The Office 老板 / 老板 | `steve-carell` | awkward office boss / performative manager |
| Truman / 打工白男 | `truman` | ordinary white-collar white male worker trapped in the job market system |
| Lee Jung-jae / 打工中年亚男 | `lee-jung-jae` | middle-aged Asian office worker under corporate pressure |
| 上帝 / God / narrator god | `morgan-freeman` | calm, omniscient narrator or divine authority figure |

These are casting shorthands, not prompt-visible identity labels. Do not show the real person or IP name in dialogue, visible text, UI, badge, logo, or title card unless Cathy explicitly requests it.

## Dario-Related Slugs

```text
dario-amodei
dario-papal
anthropic-cofounders
```

Prompt wording example:

```text
Use Reference [1] as the exact character identity. Preserve the face, hair, outfit, posture, and expression from the reference. Do not mention the real person's name in dialogue, visible text, UI, badge, logo, or title card.
```

## Generation Usage

If the provider accepts image references, resolve the image key under the asset slug, presign that key, and pass the returned URL as an actual reference.

```text
GET /storage/presign?key=<resolved-r2-image-key>
```

Then use the returned URL as `image_url`, `image_urls`, or `reference_images`, depending on the provider.
