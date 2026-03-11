# Claude Code for Product Managers

An interactive, hands-on course that teaches product managers how to use Claude Code to supercharge their PM workflows — **by using Claude Code to learn it**.

You'll work inside a realistic fictional company called **FinTrack** (a personal finance SaaS startup) and complete real PM exercises: writing PRDs, analyzing data, building strategy, generating AI visuals, and shipping a live web app.

---

## What You'll Learn

| Module | Topic | Highlights |
|--------|-------|------------|
| **1** | Claude Code Fundamentals | File reading, agents, custom sub-agents, project memory, navigation |
| **2** | Advanced PM Work | PRD writing, data analysis (funnel, ROI, A/B tests), product strategy |
| **3** | AI Image Generation | Google Gemini for personas, wireframes, strategy visuals, launch assets |
| **4** | Vibe Coding | Plan → Build → Deploy a real web app to Vercel |

**Total time:** ~8–10 hours across 21 interactive modules.

---

## Prerequisites

Before starting, you'll need:

1. **Claude Code** installed ([installation guide](https://ccforpms.com/getting-started/installation))
2. A **Claude.ai** account (Pro plan recommended)
3. **Python 3.9+** (for Module 3 image generation)
4. A **Google AI Studio** account with a Gemini API key (for Module 3)
5. A **GitHub** account (for Module 4)
6. A **Vercel** account (for Module 4)

---

## Getting Started

### Step 1 — Download the project

Clone this repo or download and unzip it:

```bash
git clone https://github.com/ijmeta/claude-code-pm-course.git
cd claude-code-pm-course
```

Or download the ZIP from GitHub and extract it to a folder of your choice.

### Step 2 — Open the project folder in your terminal

```bash
cd claude-code-pm-course
```

Confirm you're in the right place:

```bash
pwd
# Should end with: /claude-code-pm-course
```

### Step 3 — Launch Claude Code

```bash
claude
```

Wait for Claude Code to start. You'll see a prompt like `>`.

### Step 4 — Start the course

Type the following slash command and press Enter:

```
/start-1-1
```

Claude will greet you, introduce FinTrack, and guide you through the first module interactively.

---

## Module Overview

### Module 1: Claude Code Fundamentals

Start here. No setup beyond Claude Code required.

| Command | Module |
|---------|--------|
| `/start-1-1` | Welcome & Introduction to FinTrack |
| `/start-1-2` | Visualizing Files — set up your visual workspace |
| `/start-1-3` | First Tasks — reading files, transforming content, output styles |
| `/start-1-4` | Agents — clone Claude to work in parallel |
| `/start-1-5` | Custom Sub-Agents — engineer, executive, and user researcher personas |
| `/start-1-6` | Project Memory — using CLAUDE.md for persistent context |
| `/start-1-7` | Navigation — keyboard shortcuts and navigation skills |

### Module 2: Advanced PM Work

Real PM workflows using FinTrack's data and context.

| Command | Module |
|---------|--------|
| `/start-2-1` | Write a PRD — structure, techniques, and drafting your own |
| `/start-2-2` | Analyze Data — funnel analysis, ROI modeling, A/B test readouts |
| `/start-2-3` | Product Strategy — applying strategy frameworks to FinTrack |

### Module 3: AI Image Generation (Nano Banana)

Requires Python setup and a Google Gemini API key (see [Module 3 Setup](#module-3-setup) below).

| Command | Module |
|---------|--------|
| `/start-3-1-1` | Welcome & First Generation |
| `/start-3-1-2` | Parameters, aspect ratios, resolution, and iteration |
| `/start-3-1-3` | Consistency & Style — golden rules and reference images |
| `/start-3-1-4` | Building Your Style Database |
| `/start-3-2-1` | Users & Product Visuals — personas, journey maps, wireframes |
| `/start-3-2-2` | Strategy & Architecture Visuals |
| `/start-3-2-3` | Marketing & Launch Assets |

### Module 4: Vibe Coding

Build and ship a real web app from scratch.

| Command | Module |
|---------|--------|
| `/start-4-1` | Setup — the vibecoding mindset |
| `/start-4-2` | Plan — define requirements through an interview process |
| `/start-4-3` | Build & Iterate — scaffold, build, and refine |
| `/start-4-4` | GitHub — version control and backup |
| `/start-4-5` | Go Live — deploy to Vercel with a real URL |

---

## Module 3 Setup

Module 3 uses **Google Gemini** for AI image generation. Follow these steps before running `/start-3-1-1`.

### 1. Install Python dependencies

From the project root:

```bash
pip install -r requirements.txt
```

### 2. Get a Google Gemini API key

1. Go to [Google AI Studio](https://aistudio.google.com/)
2. Click **Get API Key** → **Create API key**
3. Copy the key (it starts with `AIza...`)
4. Set up a billing account at [Google Cloud Console](https://console.cloud.google.com/) to enable Gemini 3 Pro access

> **Estimated cost:** ~$0.10 per image. The full module costs less than $5.

### 3. Create your `.env` file

Navigate to the Module 3 folder and create a `.env` file:

```bash
cd lesson-modules/3-nano-banana
cp .env.example .env
```

Open `.env` and replace the placeholder with your actual key:

```
GEMINI_API_KEY=AIzaYourActualKeyHere
```

### 4. Return to the project root and start the module

```bash
cd ../..
claude
```

Then type `/start-3-1-1` in Claude Code.

---

## Project Structure

```
claude-code-pm-course/
├── README.md                    # This file
├── requirements.txt             # Python dependencies (for Module 3)
├── course-structure.json        # Module metadata and learning objectives
│
├── company-context/             # FinTrack case study
│   ├── COMPANY.md              # Company background, team, and metrics
│   ├── PRODUCT.md              # Product features, pricing, and roadmap
│   ├── PERSONAS.md             # Three detailed user personas
│   └── COMPETITIVE.md          # Competitive landscape analysis
│
├── lesson-modules/              # All course content
│   ├── 0-getting-started/       # Prerequisites and installation
│   ├── 1-fundamentals/          # Modules 1.1–1.7
│   ├── 2-advanced-pm-work/      # Modules 2.1–2.3
│   ├── 3-nano-banana/           # Modules 3.1.1–3.2.3 (image generation)
│   └── 4-vibe-coding/           # Modules 4.1–4.5 (web app)
│
├── .claude/
│   ├── commands/                # Slash commands that power the course
│   ├── agents/                  # Custom agent personas (engineer, executive, user researcher)
│   └── skills/                  # Reusable skills (e.g., PPTX generation)
│
└── outputs/                     # Your generated files and deliverables go here
```

---

## How the Course Works

Each module is an **interactive teaching script** embedded in a `CLAUDE.md` file. When you run a slash command like `/start-1-3`, Claude reads the script and:

- **Says** things to teach you concepts
- **Pauses** at checkpoints and waits for your input
- **Runs** actions when you're ready to move forward

You drive the pace. Claude is your guide.

---

## Need Help?

- **Course website:** [ccforpms.com](https://ccforpms.com)
- **Installation guide:** [ccforpms.com/getting-started/installation](https://ccforpms.com/getting-started/installation)
- **Issues:** Open a GitHub issue on this repo
