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
   - The purpose of this game is to guess the correct number within a certain number of attempts.
- [ ] Detail which bugs you found.
   - The bugs I found were starting new game, hints showing different direction, difficulty range.
- [ ] Explain what fixes you applied.
   - Fixed the New Game button by resetting the number to 1
   - Changed the hints in check_guess by changing the go higher and go lower text
   - Fixed the difficulty so it is not hard coded

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. User opens the app and selects Normal difficulty (range: 1-100, 8 attempts)
2. User enters a guess of 50 → game returns "📉 Go LOWER!"
3. User enters a guess of 25 → game returns "📈 Go HIGHER!"
4. User enters a guess of 37 → game returns "📉 Go LOWER!"
5. User enters a guess of 30 → game returns "🎉 Correct!"
6. Score updates and balloons appear on screen
7. User clicks New Game to reset all state and start fresh

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
(.venv) user ai110-module1show-gameglitchinvestigator-starter % pytest tests/
=================================== test session starts ===================================
platform darwin -- Python 3.14.5, pytest-9.0.3, pluggy-1.6.0
rootdir: /Users/jien/CodePath/AI110/ai110-module1show-gameglitchinvestigator-starter
plugins: anyio-4.13.0
collected 3 items                                                                         

tests/test_game_logic.py ...                                                        [100%]

==================================== 3 passed in 0.01s ====================================
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
