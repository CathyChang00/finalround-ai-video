# R2 Character Assets

Source checked: `r2:creative-assets/chars/`

Last checked: 2026-05-22

Use this file as a lightweight `chars/` asset slug index, not as a file-level image path list. Before generating with an R2 character, re-check the exact image key with:

```text
rclone lsf r2:creative-assets/chars/<asset-slug> --recursive
```

## Asset-First Rule

When Cathy says a character exists in R2, resolve the R2 asset and pass it as an actual image reference to the generation provider. Do not rely on prompt text to recreate a real person, company figure, or platform-sensitive identity.

In the prompt, refer to the image as `Reference [1]`, `Reference [2]`, etc. Use generic role labels such as `AI researcher`, `tech CEO`, `founder archetype`, `game doll`, or `job candidate`. Do not put sensitive real-person names, real company names, or platform-risky identity phrases into the generation prompt unless Cathy explicitly asks.

Do not paste R2 paths into the generation prompt as if the model could fetch them. R2 paths are for the agent/API layer; the prompt should only say `Reference [1]`.

## Current Chars Index

```text
ace-attorney-court
ace-attorney-elon
ace-attorney-sam
alexandr-wang
andrej-karpathy
anthropic-cofounders
avery
cursor-ceo
dario-amodei
dario-papal
elon-musk
hou-liangping
jensen-huang
jessica
jessica-canonical
lee-jung-jae
liu-yuan
mark-zuckerberg
meryl-burbank
mira-murati
modi
pete-hegseth
peter-thiel
robin-li
sam-altman
squid-game-meta-doll
sundar-pichai
truman
trump
xiao-hong
yann-lecun
```

## Dario-Related Slugs

```text
dario-amodei
dario-papal
anthropic-cofounders
```

Prompt wording example:

```text
Use Reference [1] as the exact AI researcher identity. Preserve his face, hair, outfit, posture, and calm intellectual energy. Do not mention the real person's name in dialogue, visible text, UI, badge, logo, or title card.
```

## Generation Usage

If the provider accepts image references, resolve the image key under the asset slug, presign that key, and pass the returned URL as an actual reference.

```text
GET /storage/presign?key=<resolved-r2-image-key>
```

Then use the returned URL as `image_url`, `image_urls`, or `reference_images`, depending on the provider.
