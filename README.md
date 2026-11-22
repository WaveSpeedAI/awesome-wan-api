# Awesome Wan API 🌊 — Prompts, Variants & One-Call Video Generation

> The most complete open guide to **Alibaba Wan — the open frontier AI video model (Wan 2.2 · 2.5 · 3.0)** — a community prompt library and a single API to run every variant.

<p align="center">
  <a href="https://wavespeed.ai/wan-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api"><img src="https://img.shields.io/badge/▶_Run_Wan_3.0-Get_API_Key-00E5FF?style=for-the-badge&labelColor=0B0B0F" alt="Run Wan 3.0"></a>
  <a href="https://wavespeed.ai/wan-2-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api"><img src="https://img.shields.io/badge/Wan_2.2-Try_Now-7C3AED?style=for-the-badge&labelColor=0B0B0F" alt="Wan 2.2"></a>
</p>

<p align="center">
  <b>🌊 Powered by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api">WaveSpeedAI</a> — serverless Wan API, pay-as-you-go, zero cold starts.</b><br>
  <a href="https://wavespeed.ai/wan-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api"><b>→ Get a Wan 3.0 API key</b></a> &nbsp;·&nbsp; <a href="https://wavespeed.ai/wan-2-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api"><b>→ Try Wan 2.2</b></a>
</p>

<p align="center">
  🖥️ <b>No code?</b> Generate in your browser (no setup, free to start) → <a href="https://wavespeed.ai/video-generator?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api"><b>WaveSpeedAI Video Generator</b></a>
</p>

---

> **Generate right now**
> ```bash
> npm i -g @wavespeed/cli && wavespeed login
> wavespeed run alibaba/wan-3.0/text-to-video -p "your prompt"
> ```
> No GPU, no cold start — the same endpoint powers every prompt below.

---

## 📖 Contents
1. [What is Wan?](#what-is-wan)
2. [Run it via API](#run-it-via-api)
3. [Model Variants](#model-variants)
4. [Prompt Library](#prompt-library) — 11 community prompts
5. [Related Model Guides](#related-model-guides)
6. [Contributing](#contributing)

---

## What is Wan?

**Wan** is Alibaba's frontier AI video model. Text or image in, high-motion video out, with strong prompt adherence, multi-shot consistency, and native audio on the 2.5+ line. WaveSpeed serves the full family — Wan 2.2, 2.5, 2.6, 2.7 and the latest **Wan 3.0 / 3.0-prime**.

---

## Run it via API

One endpoint, submit + poll. Swap the model path for any variant below.

```bash
curl -s -X POST "https://api.wavespeed.ai/api/v3/alibaba/wan-3.0/text-to-video" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY" -H "Content-Type: application/json" \
  -d '{"prompt": "A cinematic drone shot over misty mountains at dawn, 8k", "aspect_ratio": "16:9"}'
# → {"data": {"id": "<prediction_id>"}}

curl -s "https://api.wavespeed.ai/api/v3/predictions/<prediction_id>/result" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY"
# → status: completed → outputs: ["<url>"]
```

**[→ Get your Wan 3.0 API key](https://wavespeed.ai/wan-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api)** · pay-as-you-go, live pricing on each model page.

**Python wrapper:** [wan-3.0-api](https://github.com/WaveSpeedAI/wan-3.0-api) — one typed function per Wan 3.0 endpoint, built on the official SDK.

---

## Model Variants

All variants open in-browser with a copy-paste API snippet.

### Wan 3.0 — flagship &nbsp;[▶ API](https://wavespeed.ai/wan-3-api)
[text-to-video](https://wavespeed.ai/models/alibaba/wan-3.0/text-to-video) · [image-to-video](https://wavespeed.ai/models/alibaba/wan-3.0/image-to-video) · [reference-to-video](https://wavespeed.ai/models/alibaba/wan-3.0/reference-to-video) · [3.0-prime t2v](https://wavespeed.ai/models/alibaba/wan-3.0-prime/text-to-video)

### Wan 2.5 &nbsp;[▶ API](https://wavespeed.ai/wan-2-6-api)
[text-to-video](https://wavespeed.ai/models/alibaba/wan-2.5/text-to-video) · [image-to-video](https://wavespeed.ai/models/alibaba/wan-2.5/image-to-video) · [text-to-image](https://wavespeed.ai/models/alibaba/wan-2.5/text-to-image) · [video-extend](https://wavespeed.ai/models/alibaba/wan-2.5/video-extend)

> Full catalog: **[wavespeed.ai/wan-3-api](https://wavespeed.ai/wan-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api)**

---

## Prompt Library

11 prompts curated from the Wan creator community. Credit stays with the original author. Fill in `{...}` placeholders.

### 1. Cinematic long shot with forward tracking: In a frozen w…
*by [@azed_ai](https://x.com/azed_ai)*

```
Cinematic long shot with forward tracking: In a frozen wasteland under a black sky filled with auroras, a small squad treks across an ice ridge, their footsteps crunching over ancient wreckage. Wind howls. One pauses, raising a scope. In the valley below: dozens of beasts, dormant, coiled around a shattered mech carrier. The camera slowly tracks forward as the squad descends each step heavy, uncertain. Then one of the creatures stirs. Its eyes glow. Others follow. The ice begins to crack beneath their feet. The camera pulls upward as all hell breaks loose, beasts charging up the slope, soldiers scrambling, rifles lighting up the darkness in staccato bursts.
```

### 2. A man runs down a dark alley at night with a gun in his …
*by [@azed_ai](https://x.com/azed_ai)*

```
A man runs down a dark alley at night with a gun in his hand. Handheld 35mm medium shot tracks behind him, then whip-pans as he checks a corner. Dim streetlights, rising steam, cold breath. Slow motion pulse as he lifts the gun. He mutters, “Of course it had to be this alley…”
```

### 3. TikTok-style influencer product video
*by [@hellokaton](https://x.com/hellokaton)*

```
TikTok-style influencer video. A young woman holds up the product and talks about it, saying clearly: "Hey everyone, come try our brand-new Katon speaker — top-tier sound quality, with ChatGPT built in", shot as a low-quality amateur phone video.
```

### 4. Please enjoy, in order: GTA, Pokemon, Mario Kart, The Wi…
*by [@emollick](https://x.com/emollick)*

```
Please enjoy, in order: GTA, Pokemon, Mario Kart, The Witcher 3, Stardew Valley,  Tetris, Mortal Kombat, The Sims, & Death Stranding(!)
```

### 5. Avengers, Lord of the Rings, Transformers, Harry Potter,…
*by [@CoffeeVectors](https://x.com/CoffeeVectors)*

```
Avengers, Lord of the Rings, Transformers, Harry Potter, Top Gun, Dune, Predator, Ghostbusters, Titanic, Wakanda Forever, Batman, 300
```

### 6. Photorealistic cinematic shot of an empty pastel-pink be…
*by [@venturetwins](https://x.com/venturetwins)*

```
{ "description": "Photorealistic cinematic shot of an empty pastel-pink bedroom with white wood floors and soft daylight streaming in. A sealed Hello Kitty box with a pink bow sits in the center. It wiggles, then bursts open in a bright, sparkly puff. The room transforms instantly No text.", 
"style": "photorealistic cinematic", 
"camera": "fixed wide angle, front-facing for symmetrical reveal", 
"lighting": "soft, diffused natural light with subtle pink glow accents", 
"room": "blank pastel bedroom transformed into a Hello Kitty sanctuary", 
"elements": [ "Hello Kitty box (logo and bow visible)", "Hello Kitty bedding and pillows", 
"plushies (Hello Kitty, My Melody, Cinnamoroll, Kuromi)", "wall art or framed posters", "floating shelves with figurines and pastel accessories", "vanity with mirror and pink chair", "Hello Kitty lamp or neon sign", "heart rug or fluffy floor mat", "bow-shaped throw pillows" ], 
"motion": "box opens, cute Sanrio items explode out and assemble rapidly and precisely", "ending": "soft, cozy Hello Kitty room glowing with pink warmth and charm", 
"text": "none", 
"keywords": [ "16:9", "Hello Kitty", "Sanrio", "pastel bedroom", "fast assembly", "no text", "photorealistic", "pink explosion", "cozy kawaii" 
] 
}
```

### 7. Cinematic shot of a sunlit, empty kitchen. A sealed Chew…
*by [@venturetwins](https://x.com/venturetwins)*

```
{
"description": "Cinematic shot of a sunlit, empty kitchen. A sealed Chewy box sits in the center. It trembles, explodes open in one burst, and pet supplies rapidly assemble into place: food and water bowls, a dog bed, toys, and a bag of food. A dog runs in and flops into the bed. No text.",
"style": "cinematic",
"camera": "fixed wide angle",
"lighting": "natural warm with soft shadows",
"room": "modern kitchen with hardwood floors",
"elements": [
"Chewy box (logo visible)",
"dog food and water bowls", "
dog bed",
"dog toys (rope, ball, bone)",
"bag of dog food",
"wall hook with leash",
"dog (golden retriever)" ],
"motion": "box explodes open, dog items fly out and assemble rapidly and precisely",
"ending": "dog enters and settles happily into the bed",
"text": "none",
"keywords": [
"16:9",
"Chewy",
"pet supplies",
"fast assembly",
"dog",
"no text",
"warm lighting"
]
}
```

### 8. Photorealistic cinematic shot of an empty [futuristic-minimalist] bed…
*by [@oran_ge](https://x.com/oran_ge)*

```
Photorealistic cinematic shot of an empty [futuristic minimalist] bedroom with white wood floors and soft daylight streaming in. A sealed [a metallic tech crate stamped with the 'Orange AI' logo] sits in the center. It wiggles, then bursts open in a bright, [orange] sparkly puff. The room transforms instantly into a [futuristic tech lab] sanctuary. No text. Style: photorealistic cinematic Camera: fixed wide angle, front-facing for symmetrical reveal Lighting: soft, diffused natural light with subtle [orange] glow accents Room: blank [futuristic minimalist] bedroom transformed into a [futuristic tech lab] sanctuary Core elements: [a metallic tech crate stamped with the 'Orange AI' logo] (logo and details visible) [holographic data displays and an ergonomic command chair] plushies ([a WALL-E robot figure], [a MOSS core-unit model], [a Baymax figure], [a Tachikoma figure]) wall art or framed posters of [the J.A.R.V.I.S. interface] and their world floating shelves with figurines and [orange] accessories vanity with mirror and [orange] chair [AI-lab] lamp or a neon sign of a [a brain-neuron symbol] [circuit-board pattern] rug or fluffy floor mat [robot-helmet]-shaped throw pillows Motion: [a metallic tech crate stamped with the 'Orange AI' logo] opens, themed [artificial-intelligence] items explode out and assemble rapidly and precisely, [an anthropomorphic orange appears at the desk, speaking into a microphone] Ending: soft, cozy [futuristic tech lab] room glowing with [orange] warmth and [intelligence-and-innovation] charm Text: none Keywords: 16:9, [artificial intelligence], [sci-fi film], [orange] bedroom, fast assembly, no text, photorealistic, [orange] explosion, [intelligence and innovation]
```

### 9. A warmly lit living room at night, seen from an angle th…
*by [@umesh_ai](https://x.com/umesh_ai)*

```
A warmly lit living room at night, seen from an angle that shows the couple on a couch and part of the television screen. They sit relaxed, in the soft glow of a table lamp, surrounded by cozy decor blankets, a coffee table with snacks. The TV plays an indistinct show until it abruptly flickers. The screen now displays a live feed of the exact living room, same lighting, same posture, same moment. The couple stares in disbelief as they recognize themselves onscreen. The woman gasps, clutching the man’s arm. The candlelight trembles. They remain frozen, disturbed by the uncanny reflection.
```

### 10. Anime-style combat sequence: two rivals fight in an aban…
*by [@Artedeingenio](https://x.com/Artedeingenio)*

```
Anime-style combat sequence: two rivals fight in an abandoned factory — the camera bounces with each impact, handheld-style — steel sparks, crates shatter, and their final clash sends a shockwave through the walls
```

### 11. Playful one-shot: the LEGO logo explodes into bricks and self-assembles in mid-air
*by [@op7418](https://x.com/op7418)*

```
In a playful single-take shot, the classic LEGO logo breaks apart into countless colorful bricks that self-assemble in mid-air into an imaginative model.

Detailed scene description:

The shot opens on a pure white background with the iconic red square LEGO logo floating quietly. The entire sequence unfolds in one smooth, unbroken take. The logo suddenly trembles, then — with a click — splits into the four separate letter bricks "L-E-G-O". These letters then burst apart into a colorful "shower" of bricks raining down. Standard red, yellow, blue, and white bricks tumble and spin through the air, pulled by an invisible force, snapping together click-by-click with extreme speed and precision. The camera may follow one key brick as it finds its place. Finally, the bricks assemble perfectly in mid-air into a lively LEGO toy car.

Core idea: deconstruction of the logo and its joyful reassembly.

Camera: strict single take / one-shot, optionally with a playful slight orbit to showcase the dynamic build.

Overall style: childlike, lively, creative, satisfying.

Lighting: bright, even, cheerful studio lighting that makes the brick colors pop.

Environment: pure white or light-gray minimalist background to maximize the LEGO colors.

Core elements:

The classic LEGO logo

Colorful bricks flying after the break-up

The mid-air self-assembly process

The finished LEGO model

Sound:

Background music: light, playful melody — xylophone, percussion.

SFX: the heart of the piece is the crisp, rhythmic "click-click" of LEGO bricks snapping together.

Ending: the completed LEGO model rests perfectly at center frame. Fade to white. No text throughout.
```

*Add yours via a PR — keep the original author's credit. See [Contributing](#contributing).*

---

## Related Model Guides
Part of the WaveSpeedAI **Awesome Model** series — one guide per frontier model, all runnable through one API:

- 🎬 [awesome-seedance-api](https://github.com/WaveSpeedAI/awesome-seedance-api) — ByteDance Seedance video
- 🌊 [awesome-wan-api](https://github.com/WaveSpeedAI/awesome-wan-api) — Alibaba Wan video *(this repo)*
- ⚡ [awesome-minimax-h3-api](https://github.com/WaveSpeedAI/awesome-minimax-h3-api) — MiniMax Hailuo H3 video
- 🎞️ [awesome-kling-api](https://github.com/WaveSpeedAI/awesome-kling-api) — Kling video
- 🖼️ [awesome-seedream-api](https://github.com/WaveSpeedAI/awesome-seedream-api) — ByteDance Seedream image
- 🎨 [awesome-gpt-image-api](https://github.com/WaveSpeedAI/awesome-gpt-image-api) — OpenAI GPT Image
- 🍌 [awesome-nano-banana-api](https://github.com/WaveSpeedAI/awesome-nano-banana-api) — Google Nano Banana image

---

## Contributing
PRs welcome:
1. Reusable prompts (`{placeholders}` for swappable parts).
2. **Credit the original author** with a link.
3. No output images unless you own and can license them.

## License
[CC0-1.0](LICENSE) — text & prompts are free to use. Model outputs follow the model provider's and [WaveSpeed](https://wavespeed.ai)'s terms.

---
<p align="center"><sub>Maintained by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api">WaveSpeedAI</a> — the fastest way to run frontier image & video models via one API. <a href="https://wavespeed.ai/wan-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-wan-api"><b>Run Wan →</b></a></sub></p>
