🎙️ Day-3-of-Murf-Falcon-AI

💚 Health & Wellness Voice Companion

Welcome to Day 3 of the **10 Days of Voice Agents 2025 🚀**!
Today’s mission: Transform your voice agent into a **supportive, grounded daily wellness companion** that checks in on mood, energy, goals — and remembers past conversations!

---

✅ Day 3 Objective

Build a real-time voice companion that:

✅ Conducts short daily check-ins via voice
✅ Asks about mood, energy, stress & intentions
✅ Offers simple, realistic reflections (non-medical)
✅ Saves each check-in to a JSON log
✅ References past check-ins during future sessions

This isn’t a doctor or therapist — it’s a **friendly daily wellness buddy**.

---

🎭 Persona — Supportive Wellness Companion

Your agent should:

🗣️ Start the conversation gently
❓ Ask about feelings & energy level
🎯 Explore 1–3 goals for the day
💡 Offer small, practical suggestions
🔁 Recap the check-in and confirm

Tone example:

“Thanks for sharing. On a scale of low, medium, or high — how’s your energy today?”

The agent **must avoid** medical advice, diagnoses, or treatment guidance.

---

📥 Conversation Flow

1️⃣ Ask About Mood & Energy

Examples:

* “How are you feeling today?”
* “What’s your energy like — low, medium, or high?”
* “Anything stressing you out right now?”

2️⃣ Ask About Intentions / Goals

Simple, achievable objectives:

* “What are 1–3 things you want to get done today?”
* “Is there anything you’d like to do for yourself — rest, exercise, hobbies?”

3️⃣ Offer Grounded Reflections

Suggestions should be:

✅ Small
✅ Actionable
✅ Non-medical

Examples:

* Break big goals into smaller steps
* Take short breaks through the day
* Try a quick 5-minute walk

4️⃣ Recap & Confirm

* Mood summary
* Energy level
* Top 1–3 goals

“Does this sound right?”

If user confirms → ✅ Save the check-in.

---

💾 JSON Persistence

Each check-in is saved to:

```
/backend/wellness_log.json
```

Example entry:

```json
{
  "date": "2025-01-24",
  "timestamp": "2025-01-24T09:42:11Z",
  "mood": "Tired but okay",
  "energy": "Low",
  "objectives": ["Finish assignment", "Take a walk"],
  "summary": "Low energy, planning small goals for the day."
}
```

✅ One file
✅ Multiple entries
✅ Human-readable format

---

🔁 Using Past Data

When the next session starts, the agent should:

✅ Read the last entry
✅ Reference it once gently

Example:

“Last time you mentioned low energy. How does today compare?”

This gives the agent a sense of **continuity and memory**.

---

📍 Where to Make Changes

✅ Backend

`backend/src/agent.py`

You will:

✅ Update persona prompt
✅ Add JSON read/write helpers
✅ Implement the save tool
✅ Load previous check-ins
✅ Reference past data in the prompt

✅ The voice pipeline stays the same:
User 🎤 → Deepgram STT → Gemini LLM → Murf TTS → Audio 🔊

✨ Silero VAD manages turn-taking

✅ Frontend

No major UI changes required (optional summary display if desired)

---

🔧 Suggested Implementation Steps

✅ Step 1 — Add `wellness_log.json` helpers
✅ Step 2 — Define `WellnessEntry` model
✅ Step 3 — Create save tool
✅ Step 4 — Update system prompt
✅ Step 5 — Load + reference previous entry
✅ Step 6 — Test two sessions (to confirm memory)

---

🧪 How to Test

Ask:

“How am I feeling today? Hmm… maybe a little low energy.”

The agent should follow with:

“What’s one or two things you’d like to get done today?”

After the recap and confirmation → ✅ JSON entry saved.

Restart → Agent references the past.

---

🚀 Day 3 of #10DaysofAIVoiceAgents — I Built a Wellness Companion!

💚 My agent can now:
✅ Do guided voice check-ins
✅ Ask about mood, energy & goals
✅ Offer grounded micro-advice
✅ Save each session as JSON
✅ Remember past check-ins

#MurfAI #VoiceAI #LiveKit #Gemini #BuildInPublic #AIAgents #Wellness #TTS #STT #GenAI
