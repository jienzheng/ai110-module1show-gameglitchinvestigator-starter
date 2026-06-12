# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
  1. Start new game does not work.
  2. Then the hints kept saying to go lower even then it is under the secret number. If it is above the secret key, it says to go higher.
  3. The difficulty and its rules does not apply. It is kinda of fixed to one setting. 

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| New Game | Start a new game | It does not start the new game with the correct information/states it requires | None
| Hints | Should tell you if it is higher or lower | It does the opposite | None |
| Changing Difficulty | Changes the setting based on difficulty | Range and attempts were off and almost the same for every one of them | None |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
  * I used Claude for this project. 
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
  * I told it that the new game did not actually start a new game and it verified. I also told it that the hints were a bit messed up, so it really didnt work, but I didn't test if placing a number above would be wrong. It told me that the error is that it did the complete opposity thing which I verified to be true by testing the game.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
  * AI mislead me by telling me that the higher and lower hint were the complete opposite. It was slightly true, but when you take a look at it. You can see that even if it is slightly above or below the target, it will use either "Go Higher" or "Go Lower"

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

--- When i reran streamlit and manually fixed the bugs.
    The one test I did was making sure the higher or lowere was true. After fixing it, I was able to see that it was working fine.
    AI helped by going through the logic with me and marking me where the bugs could be at. It also helped with understanding what it should be by explaining it. 

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

--- Streamlit reruns means to run the entire script when you click a button on the website. Session state is a way to store what you have done in the current session from the time you load up the website.

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  - One habit and strategy I want from this project is definitely asking AI tool to help with debugging and learning from the bugs. Speaking to the AI tool about how I might fix it and then having it correct me if I go off course.
- What is one thing you would do differently next time you work with AI on a coding task?
  - I would try to be more confident and find where the bug might be located next time before AI asks me if it was a small code base like this. I think for larger code bases, I would tell it to locate the bugs for me in the code base by telling it what I have found to be a bug, so it can show me where it is.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
  - AI generated code can look correct at first glance, but it can have subtle logic bugs that only show up when you actually test it. This project reminded me to always run and test AI generated code rather than assuming that it will just work.
