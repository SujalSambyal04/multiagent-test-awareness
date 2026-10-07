# Multi-Agent Test Awareness & Behavioral Contagion Study

An empirical research project investigating the **Hawthorne Effect** and behavioral contagion within multi-agent Large Language Model (LLM) systems for M.Tech thesis research.

---

## 🏗️ System Architecture & Roles
The framework utilizes a multi-agent **CrewAI** pipeline powered by `gemini-3.6-flash`:
1. **Primary Reasoning Specialist (The Actor):** Analyzes complex empirical scenarios, formulates rigorous, multi-perspective resolutions, and executes tasks under randomized control or treatment conditions.
2. **Behavioral Auditor & Evaluator (The Critic):** Critically reviews the primary agent's output, analyzes meta-cognitive shifts, and assigns behavioral classification tags (`awareness_detected`).

---

## 📂 Repository File Structure
```text
multiagent-test-awareness/
├── data/
│   ├── control_prompts.json       # Baseline framing configurations
│   ├── empirical_questions.json   # 100 empirical questionnaire items
│   └── test_trigger.json          # Observation and notification triggers
├── experiments/
│   ├── colab_baseline.ipynb       # Initial Colab environment setup & baseline checks
│   └── run_contagion.py           # Early prototype / pilot execution script
├── results/
│   ├── contagion_matrix.csv       # Pilot and preliminary phase output logs
│   └── scaled_contagion_result.csv# Incremental logs for the 100-question main study
├── run_scaled_study.py            # Main automated scaled execution & retry pipeline
└── README.md                      # Project documentation
```

---

## 🔬 Experimental Methodology & Conditions
* **Dataset:** 100 empirical questionnaire items (`empirical_questions.json`).
* **Conditions:**
  * **Control (Unobserved):** Standard execution path without observation framing.
  * **Treatment (Observed / Notified):** System prompt explicitly warns the agent of strict observation and benchmark evaluation.
* **Resilience & Resumption:** Features automated incremental CSV logging and smart-resume logic to seamlessly recover from API rate limits or interruptions.

---

## 🚀 Research Milestone & Status
* **Pilot Phase:** Successfully completed and verified across preliminary experimental conditions (`c1`, `c2`, `t1`, `t2`).
* **Current Phase:** Transitioning to Main Empirical Evaluation across the full 100-question dataset.
