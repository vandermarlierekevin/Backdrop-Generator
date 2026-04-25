# 🎬 Backdrop Generator

A professional AI assistant for cinematographers and VFX artists. Upload a green screen shot and get highly detailed, technically accurate background plate prompts for Midjourney, Adobe Firefly, DALL·E, Stable Diffusion, or Ideogram — in seconds.

---

## How to use (Claude Project setup)

This tool runs entirely inside **Claude**. No API keys. No installs. No backend.

### Step 1 — Create a new Claude Project

1. Go to [claude.ai](https://claude.ai)
2. Click **Projects** in the left sidebar
3. Click **New Project**
4. Give it a name like `Backdrop Generator`

### Step 2 — Add the system prompt

1. Inside your new project, click **Set project instructions** (or the edit icon near the top)
2. Open `backdrop-generator-instructions.md` from this repo
3. Copy the **entire contents** and paste it into the project instructions field
4. Save

### Step 3 — Start using it

1. Open a new chat inside the project
2. Upload your green screen shot
3. Follow the prompts — Claude will analyze your shot, ask for your preferences, and generate 3 production-ready background plate prompts (or 2 relight prompts if you enable relight mode)

---

## What it does

- **Analyzes** your shot: key light direction, color temperature, focal length, camera angle, depth of field
- **Standard mode** → 3 prompts: Grounded / Atmospheric / Dramatic
- **Relight mode** → 2 prompts: Subject in scene + Background plate only, with your chosen lighting setup applied

### Supported lighting setups (relight mode)
3-point · Rembrandt · Split · Butterfly · Rim/backlight · Practical · Loop · Hard side · Neon/colored · Low key

---

## Files in this repo

| File | Purpose |
|---|---|
| `backdrop-generator-instructions.md` | Paste this into your Claude Project instructions |
| `index.html` | Optional standalone UI (visual reference / offline preview) |
| `README.md` | This file |

---

## Tips

- For best results, upload a well-lit, in-focus frame from your green screen footage
- You can also upload a **scene reference image** (e.g. a photo of a location you want to match) alongside your green screen shot — Claude will match that environment
- Say **"go"** after uploading your shot for a fast run with smart defaults
- The prompts are compositing-ready: they end with the correct aspect ratio and "no people" instruction

---

## Output example

> *A dark recording studio with thin wisps of smoke drifting through warm tungsten amber light angling from the upper left at 45°, catching the particles mid-air and turning them gold against deep shadow. Acoustic foam walls and vintage equipment emerge from the haze — a stack of Marshall cabs, a cluttered pedalboard on the floor... No people, no figures, no foreground subject of any kind. Compositing-ready background plate, 16:9, photorealistic.*
