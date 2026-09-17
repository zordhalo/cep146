# Lab 2: Development Environment Setup Planning

Team: The Best Team (Lucas Krawczak, Sanvi Arora)

Scenario: Building a data analysis project

Source: [team Google Doc](https://docs.google.com/document/d/1BJJi5WaSraYlk6h1eCChqj-ub_hxan09PnBrbtEalsM/edit?tab=t.0) — synced here as of 2026-09-16; the doc is the live copy while we're still editing.

## 1. Project Scenario Assignment

We chose analyzing a dataset as our scenario due to our interest in local LLM processing and data analysis using language models. The goal of this project is to produce charts, reports, and text analysis using a locally hosted large language model. Instead of a cloud API, this gives us full control over the data, removes a per-token cost, and works offline. Most companies have private data that should not be shared with API providers, so this solution will become increasingly popular.

## 2. Environment Planning

### IDE

We think the most reasonable IDE would be VS Code with a Python interpreter installed locally, along with Python's built-in data processing tools.

### Additional tools

1. **Ollama** — lets us run AI/LLM models directly on our computer. It acts as a bridge between our Python code and the local AI model.
2. **Llama3.1:8b / mistral:7b** — a quantized instruction model that actually does the summarization and Q&A.
3. **GPU** — helps run AI models faster because it can handle many calculations at the same time, improving Ollama's speed and performance.
4. **Python 3+** — main programming language for our project.
5. **Pandas** — does the cleaning, reading, and analysis.

### Hardware requirements

*(pending — not yet filled in on the source doc)*

### Team collaboration needs

*(pending — not yet filled in on the source doc)*

### Estimated setup time and complexity

*(pending — not yet filled in on the source doc)*

## 3. Setup Guide Creation

Step 1: Install Ollama locally for the given OS (macOS, Linux, Windows) from the Ollama website.

Step 2: Run `ollama pull llama3.1:8b` (or chosen AI model) to download it locally from remote.

Step 3: Double check it runs by using `ollama run [model name] "test"` to make sure the local AI model is working.

Step 4: Create a Python environment using `pip install pandas matplotlib requests`.

Step 5: Write a script that sends data summaries and/or prompts to the local endpoint `http://localhost:11434/api/generate` and checks if a response came back.

Step 6: Set up a GitHub repo for the project to store the environment plan, `requirements.txt`, and the script files.

Step 7: Begin analysis work using the local LLM (out of scope for this lab).
