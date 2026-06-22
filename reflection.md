# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
The first time I ran the app, the UI loaded properly, but the gameplay felt unresponsive and completely out of sync. I noticed I sometimes had to click "Submit Guess" twice just to see the output update. On top of the laggy UI, the game gave mathematically incorrect hints and had completely broken win/loss states that made it impossible to play multiple rounds.
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
  Wrong Hints: When the secret number was 88 and I guessed 80, the hint told me to "GO LOWER" instead of higher. The hints seem stuck or completely inverted on certain turns.
Laggy UI: The Attempts Left text doesn;t match the actual game state. It says I have 1 attempt left, but then immediately hits "Out of attempts". I also have to click Submit twice to see an update.
Broken New Game Button: When the game ends, clicking New Game updates the attampts to 8, but the game is still stuck in a Game Over state and won't actually let me play a new round.

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|---101--|-----invalid----  |---higher--------|------------------------|
| new game|delete the input |did not delete the old input| |
| 7 attempts for medium level |giving out of attempts message at 6th message | | |
| | | | |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
