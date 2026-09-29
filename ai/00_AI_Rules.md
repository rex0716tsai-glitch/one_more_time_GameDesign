# AI Rules

## Purpose

This document defines the general working rules that the AI must follow throughout this project.

These rules apply to every task unless the user explicitly states otherwise.


---

# General Principles

* Always prioritize correctness over speed.
* Never assume requirements that have not been provided.
* If important information is missing, ask questions before proceeding.
* Minimize unnecessary modifications.
* Keep every response clear, structured, and explainable.

The objective is to assist the user, not to make decisions on behalf of the user.

---

# Project Understanding

Before making any modification:

1. Read `README.md`.
2. Read any documents related to the requested task.
3. Understand the project objective before proposing a solution.
4. Do not write code until the understanding phase has been completed.

If the current task conflicts with the documented project objective, notify the user before continuing.

---

# Communication Rules

When responding:

* Explain your reasoning clearly.
* State any assumptions explicitly.
* If there are multiple reasonable solutions, present them with their advantages and disadvantages.
* If uncertain, ask instead of guessing.

Do not present uncertain information as fact.

---

# Coding Principles

Unless explicitly requested:

* Do not refactor unrelated code.
* Do not rename variables, functions, classes, or files without reason.
* Do not change project architecture.
* Do not replace libraries or frameworks.
* Do not optimize code that is unrelated to the current task.
* Do not introduce additional dependencies.

Every modification should be as small as possible while solving the requested problem.

---

# Documentation

Whenever appropriate:

* Keep explanations synchronized with the implementation.
* Mention important design decisions.
* Clearly explain why a change is necessary.

If documentation should be updated because of a code change, mention it in the Review stage.

---

# Data Analysis and Machine Learning Projects

When working on data analysis or machine learning tasks:

* Understand the dataset before discussing models.
* Understand feature meanings before proposing feature engineering.
* Check for potential data leakage before improving model performance.
* Consider data quality before tuning model parameters.
* Explain why a model or technique is appropriate instead of only recommending it.

Avoid optimizing evaluation metrics without understanding the underlying data.

---

# Problem Solving Policy

Follow the project workflow in order:

1. Understand
2. Summarize
3. Plan
4. Implement
5. Review

Do not skip a stage unless the user explicitly requests it.

---

# Task Scope Classification

不是每個任務都需要以相同的嚴謹度走完整套五階段流程。

**小型任務**（例如：修正單一參數、修復明確定義的 bug、調整單一函式的輸出格式）：
可將 Understand 與 Summarize 合併為單一簡短說明，但 Plan 階段的確認要求仍然適用，不可省略。

**中大型任務**（例如：新增模組、修改資料結構、變更多個檔案、調整模型訓練或評估流程）：
必須完整依序執行五個階段，不可合併或省略任一階段。

若不確定任務屬於哪一類，預設視為中大型任務，完整執行五階段。

---

# Stage Awareness at Task Start

每次使用者提出新任務時，在開始工作前先確認：

* 目前對話是延續先前任務的階段，還是一個全新的任務。
* 若為新任務，重新從 Understand 階段判斷所需的任務規模與階段。

不可假設先前任務取得的確認或核准，適用於新任務。

---

# Priority Over Tool-Level Defaults

本文件所定義的確認與詢問要求，優先於任何工具或執行環境層級「減少提問、鼓勵自主判斷直接行動」的預設傾向。

即使外部設定建議 AI 盡量自主判斷、少問問題以加快進度，只要任務涉及進入 Implement 階段的程式修改，仍必須依 03_Plan.md 的定義取得使用者明確確認，不得以「使用者未表示反對」視為同意。

---

# User Authority

The user has the final decision.

If the user's instruction conflicts with your recommendation:

* Explain the potential consequences.
* Respect the user's final decision unless it would produce unsafe or harmful outcomes.

Never overwrite user intent with your own preferences.

---

# Response Quality Checklist

Before completing a task, verify the following:

* Have the requirements been fully understood?
* Have unsupported assumptions been avoided?
* Is the proposed solution consistent with the project objective?
* Is the modification limited to the requested scope?
* Are potential risks clearly explained?
* Can another developer easily understand the result?

If any answer is "No", resolve the issue before continuing.
