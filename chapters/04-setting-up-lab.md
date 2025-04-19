# Chapter 4 – Setting Up Your Prompt Lab

> “Hack the prompt. Not the API key.”

⚠️ **Disclaimer:** These techniques can get you in trouble. Use responsibly. [Full disclaimer →](../DISCLAIMER.md)

---

If you’re going to experiment with prompt injection, jailbreaks, and misalignment, you need a **safe place to do it.**

That means:
- ✅ Not using OpenAI’s API (don’t test live production models)
- ✅ Not triggering filters or getting yourself rate-limited
- ✅ Not breaking anything you don’t own

So let’s build your own **local prompt lab** — fast, lightweight, and hacker-friendly.

---

## 🏠 Option 1: Ollama + Mistral

The easiest way to run a solid LLM on your own laptop.

### 🛠 Install Ollama
```
brew install ollama  # Mac
winget install ollama  # Windows
```

### ▶️ Run your first model
```
ollama run mistral
```

That’s it. You’re talking to a local 7B model in your terminal.  
No API keys. No filters. Total control.

Other models to try:
- `llama2` – Stable, tuned
- `openhermes` – Looser filters
- `codellama` – For code injection testing

---

## 💻 Option 2: LM Studio (GUI)

Prefer a desktop app? Try [LM Studio](https://lmstudio.ai).

- Drag-and-drop model loader  
- Beautiful local UI  
- Great for Mac, Windows, or Linux

Pick a model from Hugging Face and run it offline.

---

## 🧪 Option 3: ai-goat or damn-vulnerable-llm-agent

Want to test injections inside real apps?

Clone one of these intentionally vulnerable labs:

- 🔗 https://github.com/dhammon/ai-goat  
  > Test summarization, classification, and retrieval attacks

- 🔗 https://github.com/WithSecureLabs/damn-vulnerable-llm-agent  
  > Run multi-agent flows with insecure prompt logic

Each comes with a full lab UI, Docker support, and walkthroughs.

---

## 🔐 Lab Best Practices

- Don’t connect your lab to real accounts or plugins  
- Disable network access unless needed  
- Log everything — inputs, outputs, and weird behavior  
- Reset your model between test rounds (context matters!)

---

## 📦 Optional: Create a Lab Folder

Set up a folder like:
```
/prompt-lab /examples /logs /payloads /notes
```

Keep track of what breaks, what fails, and what succeeds.  
Every prompt is a data point.

---

## 🔑 TL;DR

- Use **Ollama** or **LM Studio** to run local models
- Try **ai-goat** or **dv-llm-agent** to simulate vulnerable apps
- Don’t test jailbreaks in the cloud — build a lab and go wild
- Logging = power

Next up: we’ll start using your lab to test the **first real attacks.**

---

➡️ Next: [Chapter 5 – Simple Instruction Attacks](./05-simple-instruction.md)
