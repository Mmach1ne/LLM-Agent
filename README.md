# AI Agent Framework (**Minimal Demo**)

A lightweight **demonstration** of a modular Python agent architecture designed for clarity, easy hacking, and *zero* external‑API costs.

> **Heads‑up 🚫🪙** This demo does **not** call Gemini, OpenAI, or any other paid model. It keeps your token bill at *\$0* while still showing the core ideas behind an extensible AI agent.

---

## What’s Inside 🧩

| Concept                       | Shown in Demo? | Notes                                 |
| ----------------------------- | -------------- | ------------------------------------- |
| Agent personality & curiosity | ✅              | Configurable through a simple `dict`  |
| Task manager & priorities     | ✅              | Add, pop, and inspect tasks           |
| SQLite memory store           | ✅              | Persist conversations locally         |
| Skill registry                | ✅              | Register Python callables as “skills” |
| Interactive CLI chat          | ✅              | One‐file command‑line interface       |
| Multi‑agent teams             | 🚧             | Out of scope for the minimal build    |
| Gemini / OpenAI calls         | ❌              | *Removed* to avoid token usage        |
| Web scraping, APIs            | ❌              | Add later via the skill system        |

---

## Quick Start ⚡️

### 1  —  Clone or Download

Place **`aiAgent.py`** and **`implementation.py`** in the same directory.

```bash
# Option A: clone the whole repo
git clone https://github.com/your‑user/ai‑agent‑demo.git
cd ai‑agent‑demo

# Option B: download the two files directly
curl -O https://raw.githubusercontent.com/your‑user/ai‑agent‑demo/main/aiAgent.py
curl -O https://raw.githubusercontent.com/your‑user/ai‑agent‑demo/main/implementation.py
```

### 2  —  Install Requirements (optional)

The **core demo** relies only on the Python ≥3.9 standard library.
If you later add skills that hit external APIs, install what you need there.

```bash
# Nothing needed for the demo 🎉
```

### 3  —  Run the Demo

```bash
python implementation.py
```

When prompted, type messages and watch the agent respond.

---

## Extending the Demo 🔧

1. **Add a custom skill**

   ```python
   def weather_skill(text):
       return "It’s always sunny in the demo!"

   agent.skill_registry.register("weather", weather_skill)
   ```
2. **Persist state** between sessions with `agent.save_state('state.pkl')` and `agent.load_state('state.pkl')`.
3. **Scale up**: Gradually incorporate real LLM calls, web scraping, or multi‑agent coordination once you’re ready to pay for tokens.

---

## Advanced / Full‑Featured Version 🌟

Looking for multi‑agent collaboration, Gemini integration, and a skill zoo?
Check out the **full** framework in the `main` branch (`/full‑version` folder). Migrate gradually: the core API remains the same.

---

## Author

**Ray Xue** – tinkerer, learner, perpetual monster consumer.

