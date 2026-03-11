# Module 3: AI Image Generation (Nano Banana)

**Duration:** ~2.5 hours | **Prerequisites:** Python 3.9+, Google Gemini API key

Learn how to use Google Gemini's image generation model to create professional PM visuals — personas, journey maps, wireframes, strategy diagrams, and marketing assets.

---

## Setup (Required Before Starting)

### 1. Install Python dependencies

From the project root:

```bash
pip install -r requirements.txt
```

### 2. Get a Google Gemini API key

1. Go to [Google AI Studio](https://aistudio.google.com/)
2. Click **Get API Key** → **Create API key**
3. Copy the key (starts with `AIza...`)
4. Set up a billing account at [Google Cloud Console](https://console.cloud.google.com/) to enable Gemini 3 Pro

> **Estimated cost:** ~$0.10 per image. The full module costs less than $5.

### 3. Create your `.env` file

```bash
cd lesson-modules/3-nano-banana
cp .env.example .env
```

Open `.env` and add your key:

```
GEMINI_API_KEY=AIzaYourActualKeyHere
```

### 4. Return to the project root and start

```bash
cd ../..
claude
```

Then type `/start-3-1-1` in Claude Code.

---

## Section 3.1 — Introduction to Image Generation (~1.5 hrs)

### 3.1.1 — Welcome & First Generation
`/start-3-1-1` · 10 min

API setup walkthrough and your first generated image. Claude confirms your environment is working before continuing.

### 3.1.2 — Understanding the Basics
`/start-3-1-2` · 15 min

Core parameters: aspect ratios (1:1, 16:9, 9:16), resolution levels, iteration techniques, and how prompt phrasing affects output.

### 3.1.3 — Consistency & Style
`/start-3-1-3` · 20 min

The golden rules of visual prompting. Using reference images to lock in style and generate consistent variants.

**Reference images included:**
- `Piper 1.jpg`, `Piper 2.jpg` — character consistency examples
- `Winter 1.jpg`, `Winter 2.jpg`, `Winter 3.jpg` — style iteration examples
- `style-reference.jpeg` — style matching example

### 3.1.4 — Building Your Style Database
`/start-3-1-4` · 20 min

Create a reusable library of visual styles you can apply to any image. Includes a pre-built `style-library.html` gallery and tools for extracting styles from reference images.

**Files:**
- `style-library.html` — Visual gallery of styles
- `get_style.py` — Style extraction script
- `thumbnails/` — Pre-generated style thumbnails

---

## Section 3.2 — PM Use Cases (~1 hr)

### 3.2.1 — Users & Product Visuals
`/start-3-2-1` · 25 min

Generate PM-specific visuals:
- **User personas** with realistic profile images
- **Customer journey maps**
- **Wireframe mockups** (including from hand-drawn sketches)
- **Lifestyle shots** for user empathy

**Included:** `hand-drawn-wireframe.jpg` — example input for wireframe generation

### 3.2.2 — Strategy & Architecture Visuals
`/start-3-2-2` · 20 min

Generate visuals for strategy and communication:
- System architecture diagrams
- Prioritization matrices
- Product roadmap visuals
- Framework illustrations

### 3.2.3 — Marketing & Launch Assets
`/start-3-2-3` · 20 min

Generate launch-ready marketing materials:
- App store screenshots and feature graphics
- Social media ads and announcements
- Email header images
- Press kit visuals

---

## Key Files

| File | Purpose |
|------|---------|
| `image_gen.py` | Main image generation engine (270+ lines). Handles session management, multi-turn conversations, and output saving. |
| `style_extract.py` | Analyzes reference images and extracts reusable style descriptors using Gemini 2.5 Pro vision. |
| `.env.example` | Template for your `GEMINI_API_KEY` |
| `outputs/` | Where all generated images are saved |

---

> [← Module 2](../2-advanced-pm-work/README.md) | [Back to all modules](../README.md) | [Next: Module 4 →](../4-vibe-coding/README.md)
