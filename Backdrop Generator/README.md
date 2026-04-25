# 🎬 Backdrop Generator

A professional AI tool for cinematographers and VFX artists. Set your scene preferences, attach a green screen shot, and instantly get production-ready background plate prompts for Midjourney, Adobe Firefly, DALL·E, Stable Diffusion, or Ideogram.

Runs entirely inside **Claude**. No API keys. No installs. No backend.

---

## What's new in v2

- **F-Stop selector** — Choose from f/1.2 through f/11 or let Claude match the depth of field from your shot. The f-stop directly controls how background separation and blur depth is described in every generated prompt.
- **Bokeh type** (replaces the old depth-of-field bokeh control) — Now selects the *character* of the out-of-focus rendering independently from the f-stop. Options: Circular, Swirly, Cat eye, Anamorphic oval, Soap bubble, Geometric, Nervous/busy, Soft/feathered.

---

## Setup (2 minutes)

### 1 — Create a Claude Project

1. Go to [claude.ai](https://claude.ai)
2. Click **Projects** in the left sidebar → **New Project**
3. Name it `Backdrop Generator`

### 2 — Paste the instructions

1. Inside the project, click **Set project instructions**
2. Open `backdrop-generator-instructions.md` from this repo
3. Copy the **entire file contents** and paste into the instructions field
4. Save

### 3 — Use it

1. Open a **new chat** inside the project
2. Claude automatically renders the interactive UI as an artifact
3. Set your scene preferences in the UI
4. **Attach your green screen image** to the chat
5. Click **Generate prompts** in the UI
6. Claude analyzes your shot and returns prompts rendered directly in the UI with Copy buttons

---

## How it works

`backdrop-generator-instructions.md` does two things:

- **Defines Claude's behavior** — shot analysis methodology, f-stop depth rendering, bokeh type guidance, prompt writing standards, output format rules
- **Contains the full UI code** — Claude renders the interactive HTML interface as an artifact at the start of every conversation

When you click **Generate prompts**, the UI calls `sendPrompt()` to send your settings to Claude as a structured message. Claude analyzes your image, generates the prompts, then re-renders the UI artifact with results already populated in the prompt cards — ready to copy.

---

## What it generates

**Standard mode → 3 prompts:**
- **Grounded** — Real textures, authentic materials, no atmosphere
- **Atmospheric** — Smoke, haze or dust catching the light
- **Dramatic** — Maximum shadow depth, extreme contrast

**Relight mode → 2 prompts:**
- **Subject in scene** — Subject placed in environment with chosen lighting applied
- **Background plate** — Same scene, completely empty, compositing-ready

### F-Stop settings
Match shot · f/1.2 · f/1.4 · f/1.8 · f/2.8 · f/4 · f/5.6 · f/8 · f/11

### Bokeh types
Circular · Swirly · Cat eye · Anamorphic oval · Soap bubble · Geometric · Nervous/busy · Soft/feathered

### Lighting setups (relight mode)
3-point · Rembrandt · Split · Butterfly · Rim/backlight · Practical · Loop · Hard side · Neon/colored · Low key

---

## Files

| File | Purpose |
|---|---|
| `backdrop-generator-instructions.md` | **Paste this into your Claude Project instructions** |
| `index.html` | Standalone reference copy of the UI |
| `README.md` | This file |
