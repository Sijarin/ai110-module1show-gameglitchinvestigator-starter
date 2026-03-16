# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- It didn't seem to have major error except logic error.
-  the hints were opposite and it gives one less attempt.

---

## 2. How did you use AI as a teammate?

- I used Claude.
- I prompted claude the problem after i had fixed the go higher go lower issue. I tested it again but there was still some issue so we fixed a bug where the game was secretly converting the secret number to a string on every even attempt (2nd, 4th, 6th guess, etc.). I manually tested it to be correct.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
Answer: 

---

## 3. Debugging and testing your fixes

- I manually played the game few different times with different inputs to make sure the errors are not repeated.
- After changing the app.py code line 135-142 for new game. I went and played the game won once, lost once and mid game once i clciked on the new game button and it performed as it was supposed to.

- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- Becuase the original code re-ran streamlit the whole thing, so every run it picked a new random number.

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
Answer: Like a webpage where if you touch or click anywhere it re-loads the website.

- What change did you make that finally gave the game a stable secret number?
Answer: The code if "secret" not in st.session_state: in app.py in line 92 and 93. On every rerun after that, the check fails and the existing secret is left alone.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
