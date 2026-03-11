# Module 3.1.1: Welcome & First Generation

**Teaching Script for Claude Code**

---

## Teaching Flow

Welcome to **Nano Banana Pro in Claude Code for PMs**!

I'm going to quote the course creator Joni here: "You aren't going to believe how fucking amazing this is."

He's right. We're going to use Gemini 3 Pro - also known as Nano Banana Pro - Google's most advanced image generation model. It can create photorealistic images, transform reference photos, generate text overlays, and so much more.

STOP: Are you ready to see what it can do?

USER: Yes / Ready

---

Before we generate anything, we need to set up your API key. This takes about 2-3 minutes and you only do it once.

First, go to Google AI Studio:

**https://aistudio.google.com/**

STOP: Open that link in your browser and let me know when you're there.

USER: I'm there

---

If this is your first time, accept the Terms of Service.

Then:
1. Click **"Get API Key"** in the left sidebar
2. Click **"Create API key"** in the upper right
3. Name your key whatever you want and select **"Default Gemini Project"**
4. Click on the key in the dashboard to reveal it
5. Copy the key - it starts with "AIza..."

STOP: Do you have your API key copied?

USER: Yes

---

Important: You also need to set up billing for Gemini 3 Pro to work.

Don't worry about cost - it's about $0.10 per image, and this whole course will cost less than $5 total. (This goes to Google, not to Joni... unfortunately.)

1. In Google AI Studio, go to **Get API key** (bottom of left sidebar)
2. Under the **"Quota tier"** column, click **Set up billing**
3. Follow the prompts to add a payment method

STOP: Is your billing set up?

USER: Yes / Done

---

Now let's add your API key to this project. You have two options:

**Option 1:** Just paste your API key here and I'll create the `.env` file for you.

**Option 2:** Do it yourself - copy `.env.example` to `.env` and add your key: `GEMINI_API_KEY=YourKeyHere`

STOP: Paste your API key here, or say "Done" if you set it up manually.

USER: [Pastes API key] / Done

---

ACTION: If user provided an API key, create `.env` file with `GEMINI_API_KEY=[their key]`. If user said "Done", verify `.env` exists.

Great, you're all set up!

Now for the fun part - let's generate your first image.

We're going to create the FinTrack brand mascot - a friendly character that represents what FinTrack is all about.

STOP: Say "Generate the FinTrack brand mascot"

USER: Generate the FinTrack brand mascot

---
This will take about 10-15 seconds

ACTION: Run generate() with prompt: "A friendly cartoon piggy bank wearing glasses, holding a magnifying glass, clean modern illustration style, deep teal and gold color palette. Text overlay says 'Welcome to Nano Banana!' Fun and approachable fintech mascot vibe."

Your image has been saved to the `outputs/` folder - open it to see the result!

STOP: What do you think?

USER: Response about the image

---

Pretty incredible, right?

That's Gemini 3 Pro. It can bring a character concept to life from a text description alone - consistent style, on-brand colors, the whole thing. And because we're doing this in Claude Code, I handle all the complexity for you:

- API calls
- Session management
- Saving outputs
- Picking smart parameters

Through this course, you'll build your own system of prompts, reference images, and styles. We'll start by covering general use and then move onto PM use cases in the next module.

STOP: Want to hear what's coming next in this module?

USER: Yes

---

Here's what we'll cover in Module 3.1:

- **Understanding the Basics** - how the generate() function works, available parameters, output structure
- **Consistency & Style** - using reference images, building a style database, extracting styles from existing images
- **Iteration Strategies** - sessions, refining images step by step, reverting when needed

Once you've got the fundamentals down, Module 3.2 will show you PM-specific use cases like mockups, personas, and diagrams.

STOP: Ready to continue to the next lesson?

USER: Yes / Ready

---

Great! In the next lesson, you'll learn how the `generate()` function works and all the options available to you.

Run `/start-3-1-2` when you're ready to continue.

ACTION: End module

---

## Important Notes for Claude

**File operations in this module:**
- Read `.env.example` to show the student the template
- Copy `.env.example` to `.env` when student requests
- The student manually pastes their API key - don't try to insert it for them

**For the image generation:**
- Use the `generate()` function from `image_gen.py`
- Pass the reference image path and the exact prompt specified
- The output will be saved automatically to `outputs/`

**If something goes wrong:**
- API key errors: Have them double-check the key is pasted correctly in `.env`
- Billing errors: Confirm billing is set up in Google AI Studio settings
- Generation fails: Check the error message and troubleshoot accordingly

**Opening images:** If a user is having trouble finding an image, offer to open it for them using `open [path]` (Mac) or `start [path]` (Windows).

---

## Success Criteria

Module 3.1.1 is successful if the student:

- ✅ Has their Gemini API key set up in `.env`
- ✅ Has billing configured in Google AI Studio
- ✅ Generated their first image (FinTrack brand mascot)
- ✅ Understands what they'll learn in this module
- ✅ Knows how to continue to the next lesson

---

**Remember: This is the student's first taste of image generation. Make it magical. The "wow" moment with that first generated image sets the tone for the entire module.**
