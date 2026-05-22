# R2 Character Assets

Source checked:

- `r2:creative-assets/chars/`
- `r2:creative-assets/influencer/`

Last checked: 2026-05-22

Use this file as a lightweight index, not as a permanent source of truth. Before generating with an R2 character, re-check the exact path with `rclone lsf r2:creative-assets/chars/<asset-slug> --recursive`.

## Asset-First Rule

When Cathy says a character exists in R2, resolve the R2 asset and pass it as an actual image reference to the generation provider. Do not rely on prompt text to recreate a real person, company figure, or platform-sensitive identity.

In the prompt, refer to the image as `Reference [1]`, `Reference [2]`, etc. Use generic role labels such as `AI researcher`, `tech CEO`, `founder archetype`, `game doll`, or `job candidate`. Do not put sensitive real-person names, real company names, or platform-risky identity phrases into the generation prompt unless Cathy explicitly asks.

Default version selection: use the newest dated folder. If two versions exist, prefer `20260521/frames/v01.png` over `20260520/frames/v01.png` unless Cathy asks for the older look.

## Current Chars Index

```text
ace-attorney-court/20260520/frames/v01.png
ace-attorney-elon/20260520/frames/v01.png
ace-attorney-sam/20260520/frames/v01.png
alexandr-wang/20260520/frames/v01.png
alexandr-wang/20260521/frames/v01.png
andrej-karpathy/20260520/frames/v01.png
andrej-karpathy/20260521/frames/v01.png
anthropic-cofounders/20260520/frames/v01.png
anthropic-cofounders/20260521/frames/v01.png
avery/canonical.png
avery/canonical/avery-canonical.png
cursor-ceo/20260520/frames/v01.png
cursor-ceo/20260521/frames/v01.png
dario-amodei/20260520/frames/v01.png
dario-amodei/20260521/frames/v01.png
dario-papal/20260520/frames/v01.png
dario-papal/20260521/frames/v01.png
elon-musk/20260520/frames/v01.png
elon-musk/20260521/frames/v01.png
hou-liangping/20260520/frames/v01.png
hou-liangping/20260521/frames/v01.png
jensen-huang/20260520/frames/v01.png
jensen-huang/20260521/frames/v01.png
jessica/20260407_front-headshot/frames/v01.png
jessica-canonical/20260413_finalround/frames/jessica_canonical_768.jpg
lee-jung-jae/20260521/frames/v01.png
liu-yuan/20260520/frames/v01.png
liu-yuan/20260521/frames/v01.png
mark-zuckerberg/20260520/frames/v01.png
mark-zuckerberg/20260521/frames/v01.png
meryl-burbank/20260521/frames/v01.png
mira-murati/20260520/frames/v01.png
mira-murati/20260521/frames/v01.png
modi/20260520/frames/v01.png
modi/20260521/frames/v01.png
pete-hegseth/20260520/frames/v01.png
pete-hegseth/20260521/frames/v01.png
peter-thiel/20260521/frames/v01.png
robin-li/20260520/frames/v01.png
robin-li/20260521/frames/v01.png
sam-altman/20260520/frames/v01.png
sam-altman/20260521/frames/v01.png
squid-game-meta-doll/20260521/frames/v01.png
sundar-pichai/20260520/frames/v01.png
sundar-pichai/20260521/frames/v01.png
truman/20260521/frames/v01.png
trump/20260520/frames/v01.png
trump/20260521/frames/v01.png
xiao-hong/20260520/frames/v01.png
xiao-hong/20260521/frames/v01.png
yann-lecun/20260520/frames/v01.png
yann-lecun/20260521/frames/v01.png
```

## Dario-Related Defaults

- Standard Dario-style reference: `chars/dario-amodei/20260521/frames/v01.png`
- Papal / ceremonial Dario-style reference: `chars/dario-papal/20260521/frames/v01.png`
- Anthropic cofounders group reference: `chars/anthropic-cofounders/20260521/frames/v01.png`

Prompt wording example:

```text
Use Reference [1] as the exact AI researcher identity. Preserve his face, hair, outfit, posture, and calm intellectual energy. Do not mention the real person's name in dialogue, visible text, UI, badge, logo, or title card.
```

## Generation Usage

If the provider accepts image references, presign the R2 key and pass the URL as an actual reference:

```text
GET /storage/presign?key=chars/dario-amodei/20260521/frames/v01.png
```

Then use the returned URL as `image_url`, `image_urls`, or `reference_images`, depending on the provider.

Do not paste the R2 path into the generation prompt as if the model could fetch it. The path is for the agent/API layer; the prompt should only say `Reference [1]`.

## Current Influencer Index

These are candidate / influencer identity folders. Use them when Cathy asks for an influencer, girl, ABG, candidate, graduation student, street-interview character, or recurring FinalRound protagonist.

```text
01-chaeyoung/
02-manon/
03-sophia/
04-yoonchae/
05-haerin/
06-minji/
07-hana/
08-jiyoon/
09-linh/
10-beach-girl/
11-nara/
12-zara/
13-kai/
14-claire/
15-valentina/
16-supermodel/
ABG girl/
Jessica (abg)Instagram/
korean-girl/
```

For influencer folders, re-check the folder before generation and choose a clear face/image file as `Reference [1]`; do not rely on the folder name alone.
