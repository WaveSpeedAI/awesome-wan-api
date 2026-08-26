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

### 3. tiktok 风格的影响者视频
*by [@hellokaton](https://x.com/hellokaton)*

```
tiktok 风格的影响者视频。一位年轻的中国女性举起并谈论这个产品，她用清晰的中文说到："欢迎大家来尝试我们家新出的 katon 音响，音质超一流，支持 ChatGPT"，用手机拍摄的低质量业余视频。
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

### 8. Photorealistic cinematic shot of an empty [未来主义极简风格] bed…
*by [@oran_ge](https://x.com/oran_ge)*

```
Photorealistic cinematic shot of an empty [未来主义极简风格] bedroom with white wood floors and soft daylight streaming in. A sealed [印有'Orange AI'标志的金属科技箱] sits in the center. It wiggles, then bursts open in a bright, [橙色] sparkly puff. The room transforms instantly into a [未来科技实验室] sanctuary. No text. 风格: photorealistic cinematic 镜头: fixed wide angle, front-facing for symmetrical reveal 灯光: soft, diffused natural light with subtle [橙色] glow accents 房间: blank [未来主义极简风格] bedroom transformed into a [未来科技实验室] sanctuary 核心元素: [印有'Orange AI'标志的金属科技箱] (logo and details visible) [全息数据显示屏和人体工学指挥椅] plushies ([瓦力机器人模型], [MOSS核心单元模型], [大白模型], [塔奇克马模型]) wall art or framed posters of [J.A.R.V.I.S.界面] and their world floating shelves with figurines and [橙色] accessories vanity with mirror and [橙色] chair [AI实验室] lamp or a neon sign of a [大脑神经元符号] [电路板图案] rug or fluffy floor mat [机器人头盔]-shaped throw pillows 动态: [印有'Orange AI'标志的金属科技箱] opens, themed [人工智能] items explode out and assemble rapidly and precisely, [一只拟人化的橘子出现在桌前对着麦克风说话] 结局: soft, cozy [未来科技实验室] room glowing with [橙色] warmth and [智能与创新] charm 文本: none 关键词: 16:9, [人工智能], [科幻电影], [橙色] bedroom, fast assembly, no text, photorealistic, [橙色] explosion, [智能与创新]
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

### 11. 在一个充满趣味的一镜到底镜头中，经典的乐高标志将分解为无数色彩斑斓的积木颗粒，并在空中自动拼搭成一个充满想象力的…
*by [@op7418](https://x.com/op7418)*

```
在一个充满趣味的一镜到底镜头中，经典的乐高标志将分解为无数色彩斑斓的积木颗粒，并在空中自动拼搭成一个充满想象力的模型。

详细场景描述:

画面始于一个纯白背景前，标志性的红色方形乐高（LEGO）标志静静悬浮。整个过程将由一个流畅、不间断的镜头完成。 标志突然轻微晃动，随后“咔”的一声，它分解为“L-E-G-O”四个独立的字母积木。紧接着，这四个字母再次爆开，化作一场五彩斑斓的积木“阵雨”倾泻而下。这些红、黄、蓝、白的标准积木颗粒在空中飞舞、旋转，被一股无形的力量牵引，以极快的速度和精准度相互“咔哒、咔哒”地扣合在一起。镜头可以跟随其中一块关键积木，看它如何找到自己的位置。最终，这些积木在空中完美地拼装成一个活泼的乐高小汽车模型。

核心创意: 标志的解构与充满乐趣的重组。

镜头与运镜: 严格的一镜到底（Single take / One-shot），可以带有趣味性的轻微环绕运镜，以展现拼搭过程的动态感。

整体风格: 充满童趣、活泼、有创造力、令人满足。

灯光: 明亮、均匀、欢快的影棚灯光，让积木的色彩显得格外鲜艳。

环境: 纯白或浅灰色的极简背景，以最大限度地突出乐高积木的色彩。

核心元素:

经典的乐高标志

分解后飞舞的各色积木颗粒

空中自动拼搭的过程

最终成型的乐高模型

音效:

背景音乐: 轻快、俏皮的旋律，可使用木琴、打击乐等乐器。

特效音: 整个过程的核心是乐高积木相互扣合时清脆、悦耳、富有节奏感的“咔哒”声。

结尾: 拼搭完成的乐高模型完美地静置在画面中央。画面淡出为白色。全程无任何文字。
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
