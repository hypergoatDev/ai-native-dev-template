# 🚀 AI-Native Software Factory Template

This template provides a zero-setup, fully configured GitHub Codespace and a strict, professional methodology for building software alongside an AI coding agent (like GitHub Copilot).

It enforces a "Plan, Pause, Execute" workflow, preventing the AI from hallucinating, making unauthorized architectural changes, or committing broken code to your main branch.

## 📋 Prerequisites
1. A free GitHub account.
2. An active GitHub Copilot subscription.

## 🛠️ How to Start (Zero Local Setup)
1. Click the green **"Use this template"** button at the top of this repository and create your own repo.
2. In your new repo, click the green **"Code"** button, select the **"Codespaces"** tab, and click **"Create codespace on main"**.
3. Wait ~60 seconds for the browser editor to load. Copilot Chat will open automatically.
4. **Copy the prompt below**, paste it into Copilot Chat, fill in your idea, and hit Enter!

---

### 🤖 Day 1 Bootstrap Prompt
*(Copy everything below this line into Copilot Chat)*

Act as my Lead Architect. Please read `docs/agent-protocol.md` to understand our strict development workflow. 

My idea for this project is: **[DESCRIBE YOUR APP/IDEA HERE IN 2-3 SENTENCES]**.

Please initialize our project by doing the following in order:
1. **Branching:** Create and checkout a new git branch called `setup/initial-architecture`. Do not commit to `main`.
2. **Readme:** Overwrite `README.md` with a high-level project overview, tech stack recommendation, and core features based on my idea.
3. **Planning:** Scaffold `docs/implementation-plan.md` into 4-5 logical, step-by-step phases.
4. **Current Step:** Set `docs/current-step.md` to focus entirely on Phase 1, Step 1.
5. **Questions:** Identify any immediate technical unknowns and log them as `[OPEN]` in `docs/development-questions.md`.
6. **Pause:** Ask for my approval before proceeding to any code generation.
