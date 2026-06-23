# AI Interactions Log

> **Stretch features only.** Only fill in the sections that apply to stretch features you attempted. If you did not attempt a stretch feature, leave its section blank or delete it. This file is not required for the core project.

---

## Agent Workflow (SF8)

> Document your experience using an AI agent (e.g., Cursor Agent, Claude, Copilot) to make multi-step changes autonomously.

**Agent used:** 
Claude Code inside VS Code.

**What task did you give the agent?**

I gave it the buggy AI-generated guessing game and asked it to investigate the glitches and explain the underlying logic causing each one, and fix all of the problems in
the code. 
Specifically, I reported three symptoms:
1. In Normal difficulty, typing `101` told me to keep guessing instead of giving an
   out-of-range error.
2. Clicking **New Game** did not clear my previous guess out of the input box.
3. I was getting fewer turns than the "Attempts allowed" number shown in the sidebar.

**What did the agent do?**

- Read both files (`app.py` and `logic_utils.py`) and Diagnosed the root cause of each glitch and fixed the glitches. 
 

**What did you have to verify or fix manually?**

- I just read the given code from AI and made sure it is understandle and clean. 

## Test Generation (SF7)

> Document how you used AI to help generate or improve tests.

| Edge Case | Prompt Used | AI-Suggested Test | Did It Pass? | Your Reasoning |
|-----------|-------------|-------------------|--------------|----------------|
| | | | | |
| | | | | |
| | | | | |

---

## Linting & Style (SF9)

> Document your use of AI for linting or code style improvements.

**Prompt used:**

```
<!-- Paste the prompt you gave the AI -->
```

**Linting output before:**

```
<!-- Paste relevant linter warnings/errors -->
```

**Changes applied:**

<!-- Describe what you changed based on the AI's suggestions -->

---

## Model Comparison (SF11)

> Compare two AI models on the same task.
only one model used 

**Task given to both models:**

<!-- Describe what you asked each model to do -->

| | Model A | Model B |
|-|---------|---------|
| **Model name** | | |
| **Response summary** | | |
| **More Pythonic?** | | |
| **Clearer explanation?** | | |

**Which did you prefer and why?**

<!-- Your conclusion -->
