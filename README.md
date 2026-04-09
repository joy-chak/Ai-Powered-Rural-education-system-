# AI Tutor for Rural Students

This project is an **n8n workflow** that acts as an AI-powered tutor for students with limited internet access. It generates lessons, evaluates answers, and tracks student progress.

---

##  Features

-  Generates short, simple lessons based on topic and grade
-  Asks one question per lesson
-  Evaluates student answers
-  Provides feedback and encouragement
-  Tracks student progress (score, attempts, level)
-  Adapts difficulty (Beginner → Intermediate → Advanced)

---

##  Tech Stack

- n8n (workflow automation)
- Google Gemini (AI model)
- Data Tables (student database)

---

##  Workflow Overview

1. **Receive Input**
   - Student sends:
     ```json
     {
       "student_id": "123",
       "topic": "fractions",
       "grade": "5"
     }
     ```

2. **Check Student**
   - If new → create student
   - If existing → fetch data

3. **Generate Lesson**
   - Short explanation (2–3 lines)
   - One question

4. **Store Lesson**
   - Saves lesson + correct answer

5. **Student (Answer)**
   ```json
   {
     "student_id": "123",
     "answer": "your answer"
   }
