#  Agent of Justice: Intelligent Courtroom Simulation
Welcome to **Agent of Justice**, an intelligent courtroom simulation project built using LLM agents (like judges, prosecutors, defense attorneys, witnesses, and jury). This simulation mimics a realistic court trial workflow using multi-agent communication, legal reasoning, and dynamic decision-making.

---

## 📁 Project Structure

This repo contains 3 main Jupyter Notebooks:

| File | Description |
|------|-------------|
| `justice1.0.ipynb` | : A basic courtroom simulation with statically defined roles (Judge, Prosecutor, Defense, Plaintiff, etc. |
| `justice1.1.ipynb` | Improved version using a JudgeDrivenTrial class.. |
| `justice1.2.ipynb` |  final submission to the induction task. |

---

## Optimized Notebook (Judge-Only Verdict Shortcut)
	•	Context: Since justice1.2.ipynb takes a long time to execute, we created an alternate lightweight notebook where only the Judge reads the case summary and delivers a verdict directly.
	•	Goal: Provide a faster solution for demo or testing purposes, without running the entire trial phases.

## justice1.0ipynb - Baseline Simulation (No Dynamic Agent Creation)
	•	Description: A basic courtroom simulation with statically defined roles (Judge, Prosecutor, Defense, Plaintiff, etc.).
	•	Key Features:
	•	Linear trial flow: opening, examination, closing, verdict.
	•	Agents use LLMs for generating dialogue (Groq & HF).
	•	No support for adding roles dynamically.
	•	Limitation: Agent roles must be hardcoded. Cannot add new agents during runtime.

##  justice1.1.ipynb - JudgeDrivenTrial with Dynamic Agent Creation
	•	Description: Improved version using a JudgeDrivenTrial class.
	•	Key Features:
	•	Dynamic agent creation (e.g., witnesses, custom characters).
	•	Centralized judge control over trial flow.
	•	Modular phases: opening, direct/cross-examination, jury deliberation, final verdict.
	•	Cleaner code structure using object-oriented design.
	•	Highlight: You can add agents like witnesses dynamically using .add_agent().

## justice1.2.ipynb — made for kaggle submission

  • this code was modified to give the final verdict as 0 or 1
  • tried to implement concurrent.futures but rate limit was exceeded
  • finally this failed and i had to make another notebook that takes in whole case_summary and judge inspects it to give final verdict directly wihout any intermediate         discussions

## tech stack
	•	Python
	•	Groq API (LLaMA3 model) for smart dialogue
	•	HuggingFace fallback model for responses
	•	Object-Oriented Programming (OOP) for simulation architecture
	•	Kaggle + Jupyter environment for development and testing

## how to run 
	1.	Clone or download this repo.
	2.	Install required packages: requests, huggingface_hub, regex.
	3.	Run the notebooks in order:
	•	justice1.0.ipynb: Learn the basics.
	•	justice1.1.ipynb: Explore dynamic agent logic.
	•	justice1.2.ipynb: Execute full trial (longer runtime).

## developed by Adithya 
## part of induction task


