# 🎮 Game Glitch Investigator: The Impossible Guesser
## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
It's a number-guessing game.The app picks a secret number within a range set by difficulty — Easy 1–20, Normal 1–100, Hard 1–50 — and the player tries to guess it within a limited number of attempts (Easy 6, Normal 8, Hard 5). After each guess the game gives a "go higher / go lower" hint, tracks a score, keeps a guess history, and ends on a win or when attempts run out.
The exercise is to investigate the glitches, explain the underlying logic causing them, and fix them.
- [ ] Detail which bugs you found.
Out-of-range guesses were accepted.
"New Game" didn't clear the input box.
Players got fewer attempts than the sidebar advertised. 
- [ ] Explain what fixes you applied.
Range validation — in parse_guess(), after confirming the input is an integer, reject anything below low or above high and return a clear out-of-range error, so invalid numbers like 101 never reach check_guess().

Clear input on New Game — in the New Game handler, also clear the guess_input_{difficulty} key from st.session_state (alongside the existing state resets) so the box empties when a new game starts.

Count only valid attempts — move the st.session_state.attempts += 1 increment to after parse_guess() succeeds, so only legitimate, in-range guesses consume a turn and the player gets the full count shown in the sidebar.


## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. <!-- Describe this step -->
2. <!-- Describe this step -->
3. <!-- Describe this step -->
4. <!-- Describe this step -->
5. <!-- Add more steps as needed -->

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->![alt text](<Screenshot 2026-06-22 200510.png>)

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# pytest tests/
# ========================= X passed in 0.XXs =========================
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
