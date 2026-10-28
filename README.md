# LearnLoop AI — Adaptive Learning Platform for Python

**LearnLoop AI** is a responsive, AI-powered adaptive learning web application built for hackathon evaluation and personalized Python education.

It implements a continuous, pedagogical learning loop:
**Diagnostic Quiz → Weak Concept Detection → Personalized Explanation → Recommended Resources → Adaptive Practice → Retest → Knowledge DNA Update**.

---

## 🌟 Key Architecture & Highlights

- **Tech Stack:** React 19, TypeScript, Vite, Tailwind CSS, Lucide icons, Canvas Confetti.
- **Offline-First & Zero-Cost:** Full client-side adaptive engine using `localStorage` persistence. Zero external API keys, zero paid LLM costs, and zero network lock-in.
- **Optional FastAPI + SQLite Backend:** Fully compatible with local health check and database storage.
- **5 Python Core Concepts Taught:**
  1. `variables` — **Variables & Data Types**: numbers, float division `/`, string concatenation, mutable lists, dictionary `.get()`, reference semantics vs copying.
  2. `conditions` — **Conditional Logic**: `if`, `elif`, `else`, comparison `==`, logical `and`/`or`/`not`, truthiness/falsiness of empty collections, operator precedence.
  3. `loops` — **Loops & Iteration**: `for`, `while`, exclusive `range(start, stop, step)`, `break`, `continue`, `while-else` construct.
  4. `nested_loops` — **Nested Loops & Grids**: 2D coordinate systems `(row, col)`, matrix traversal, inner loop state resets, dependent ranges, diagonal summation.
  5. `functions` — **Functions & Scope**: `def`, default arguments, keyword vs positional parameters, `return` vs `print`, local variable shadowing, mutable default argument traps.

---

## 🚀 Complete Feature Suite

1. **Core Learning Loop (Highest Priority):**
   - Step 1: 5-Domain Baseline Diagnostic Assessment.
   - Step 2: Algorithmic Gap Detection (identifies concept with score < 50% and isolates root misconception).
   - Step 3: Personalized Analogy Explanation tailored to student's chosen hobby (Cricket, Gaming, Music, Cooking) and Persona.
   - Step 4: Recommended Remedial Resources (curated official Python guides and interactive notes).
   - Step 5: Calibrated Adaptive Practice (3 targeted practice problems at Level 1 or 2).
   - Step 6: Retest Weak Concept (3-question retest measuring immediate learning gain).
   - Step 7: Knowledge DNA & Dashboard Update (displays Before vs After mastery delta and schedules 1-day revision).

2. **Student Dashboard:**
   - Real-time KPIs clearly distinguishing:
     - **Estimated Concept Mastery** (rolling window of latest 5 attempts)
     - **Lifetime Measured Quiz Accuracy** (total correct / total attempted across lifetime)
     - **Programmer Level & Monotonic XP** (independent from skill mastery)
     - **Active Habit Streak** (flame multiplier)
   - Visual step-by-step progress stepper for the 7-step cycle.
   - Ebbinghaus Spaced Repetition reminders (1, 3, 7, 14 days) with 1-click "Review Now".
   - Concept mastery radar overview for all 5 domains.
   - Daily quest riddle with +60 XP claimable reward.

3. **Adaptive Practice Arena & Retest:**
   - Filter by topic or test all 5 concepts.
   - **Auto-Adaptive Mode:** Automatically evaluates student's mastery:
     - `< 50% Mastery`: Level 1 Foundational questions + remedial resources.
     - `50% – 79% Mastery`: Level 2 Guided practice.
     - `80%+ Mastery`: Level 3 Mastery challenge questions.
   - **Retest Weak Concepts Mode:** Instantly targets only concepts with detected gaps (< 50%).
   - Multi-level progressive hints (concept nudges & code tracing).
   - Comprehensive syntax feedback and difficulty recalibration.

4. **Blitz Quiz (60s Sprint or Untimed):**
   - Configurable timer: 30s, 60s, or Untimed Practice.
   - Dynamic combo streak multipliers (1.0x → 1.5x → 2.0x → 2.5x).
   - Instant visual feedback and final score breakdown with XP rewards.

5. **Bug Hunter (Interactive Debugging Lab):**
   - Predefined Python syntax and logic challenges (never executes arbitrary code).
   - Dual-terminal view: Buggy Python script vs Expected console output.
   - Multiple-choice repair options with verified explanations and XP bounties.

6. **Knowledge DNA Concept Mastery Map:**
   - 5-domain visual matrix.
   - Visual dots representing the rolling latest 5 attempts.
   - Subtopic status nodes (Mastered, Learning, Weak).
   - Common detected misconceptions and concrete remedies.

7. **Personalized Tutor with 4 Personas:**
   - 🌟 **Friendly Mentor:** Empathetic, supportive, growth-mindset framing.
   - 🔬 **Feynman Explainer:** Plain English, intuitive physical analogies, zero jargon.
   - ⚔️ **Gamer / Strategist:** RPG quests, HP/mana, cooldowns, DPS, and skill trees.
   - 🏛️ **Socratic Tutor:** Thought-provoking questions, progressive hints, and guided reflection.
   - Instant zero-cost offline intelligence.

8. **Hobby-Based Analogies (20 Curated Blueprints):**
   - 🏏 **Cricket:** Match scoreboards, DRS reviews, bowling an over, 20-over innings, helicopter shot routines.
   - 🎮 **Gaming:** Character HUD stats, shield checks, main while game loop, 2D tile dungeon rendering, spell macros.
   - 🎵 **Music:** Audio parameters, major/minor chord branching, 4/4 drum loops, song bars & beats, chorus presets.
   - 🍳 **Cooking:** Recipe measurements, taste checks, stirring batter loops, cupcake baking trays, secret sauce recipes.

9. **Virtual Peer Study Lounge (Scripted Simulation):**
   - Scripted virtual peers: **Alex** (Beginner), **Sam** (Intermediate), and **Dr. Maya** (Facilitator).
   - Prominently labeled with a disclaimer banner: `[SCRIPTED VIRTUAL PEERS • SIMULATION MODE — Not connected to live AI]`.
   - Threaded discussions, upvoting, and simulated peer reply generator.

10. **Curated Resources:**
    - Valid, official educational links: Python Software Foundation Tutorial, Real Python guides, freeCodeCamp cheatsheets.
    - Interactive Python Core syntax reference with 1-click copy.

11. **Certified Progress Report & Spaced Repetition Scheduling:**
    - Spaced repetition schedules at **1, 3, 7, and 14 days** based on practice timestamps.
    - Printable PDF / transcript layout.
    - **Export Progress JSON:** 1-click download of student state, attempt logs, and revision schedule.

12. **Preferences & Onboarding:**
    - Student name & username editing.
    - Default hobby & persona selection.
    - Onboarding Tour modal walkthrough.
    - Demo reset utility.

---

## 🏃 Quick Start Guide

### 1. Run the Frontend (UI + Adaptive Engine)

Open PowerShell in the `frontend` directory:

```powershell
cd C:\Users\piyus\OneDrive\Desktop\PROJECT\frontend
npm run dev
```

> **Note on Windows PowerShell:** If your execution policy blocks `npm`, run:
> ```powershell
> npm.cmd run dev
> ```
> Open the URL Vite outputs: **http://localhost:5173**

### 2. Run the Production Build & Checks

```powershell
cd C:\Users\piyus\OneDrive\Desktop\PROJECT\frontend
npm.cmd run lint     # 0 errors, 0 warnings
npm.cmd run build    # Production build (dist/)
npm.cmd run preview  # Preview production build on http://localhost:4173
```

### 3. Optional: Run the FastAPI Backend

If you wish to run the optional backend alongside the UI:

```powershell
cd C:\Users\piyus\OneDrive\Desktop\PROJECT\backend
.\.venv\Scripts\Activate.ps1
python -m uvicorn app.main:app --reload --host 127.0.0.1 --port 8000
```

To run backend tests:
```powershell
cd C:\Users\piyus\OneDrive\Desktop\PROJECT\backend
.\.venv\Scripts\python.exe -m pytest
```

---

## 🌐 Deployment Instructions

### Deploy to Vercel
1. Push this repository to GitHub.
2. In the Vercel dashboard, click **Add New Project** and import the repository.
3. Configure the build settings:
   - **Root Directory:** `frontend`
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
4. Click **Deploy**. LearnLoop AI will be live with full offline-first client persistence!

### Deploy to Netlify
1. Connect repository in Netlify.
2. Set **Base directory** to `frontend`.
3. Set **Build command** to `npm run build`.
4. Set **Publish directory** to `dist`.
5. Deploy site.

---

## 🧪 Verified Test Results

- `npm run lint`: **0 errors, 0 warnings** across all 24 source files.
- `npm run build`: **Built in < 1 second** (`dist/` ready for static deployment).
- `pytest` (backend): **7 passed in 0.42s** (100% pass rate).
- Production preview server: **HTTP Status 200 OK**.
