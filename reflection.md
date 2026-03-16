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
One AI suggestion that was misleading was about moving the debug expander in the Streamlit script. The AI said the expander was at line 115 and reading `st.session_state.score` before the submit logic updated it, which supposedly caused the score to show one guess behind. It suggested moving the expander to the bottom of the script. After testing, I reverted the change and the linter placed it back at line 115, and the program still worked correctly. This showed the issue was not actually caused by the expander’s position. I verified this by running the app and seeing that the score updated properly.

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
Answer: One habit I want to reuse is testing the code after every change suggested by AI. Instead of assuming the suggestion is correct, I ran the program and checked the output to make sure it actually worked. I do the git portion myself.
  
- What is one thing you would do differently next time you work with AI on a coding task?
Answer: Next time I would be more specific with my prompts and provide more context about the code and also make test cases for all errors so i dont have to manually check everything.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
Answer: This project showed me that AI-generated code can be helpful for initial ideas and debugging and syntax, but it should not be trusted blindly. It is important to review and test everything the AI suggests before using it or pushing a project.
