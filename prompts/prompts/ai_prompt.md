Prompt: Build the AI Learning Assistant for Feyntech

Goal:
Add AI-powered educational tools inside each room to help simplify learning, ask questions, and explain topics.

Required AI Actions:
1. Explain Simple

Input: text from user

Output: simplified explanation using the Feynman technique

Very clear, easy wording

No jargon

2. Generate Questions

Generate 3–5 questions about the topic

Questions should help the student check understanding

Mix easy and medium levels

3. Feedback / Correct Understanding

User inputs a short explanation

AI checks:

correctness

missing parts

misunderstandings

Returns feedback in a friendly tone

4. Translate

Translate explanation into any chosen language

Maintain clarity and simple tone

Backend Requirements:

Create AI controller with routes:

POST /ai/explain_simple
POST /ai/generate_questions
POST /ai/get_feedback
POST /ai/translate_text


Each route:

receives text

sends it to Cayu AI Blocks (LLM)

returns JSON response

updates the UI with the answer

Frontend Requirements:

Each AI button must trigger correct backend action

Show loading indicator

After receiving response → render text on screen
