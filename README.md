\# 🥈 Buy or Wait? — AI Financial Agent



\## 2nd Place — HackerRank Orchestrate September 2026



\[HackerRank Orchestrate — 2nd Place](screenshots/ranking.png)



This project placed \*\*2nd globally\*\* in the HackerRank Orchestrate September 2026 challenge.



\### Challenge



Build an AI-powered financial agent that determines whether a user can safely afford a requested expense.



The agent needs to reason about:



\- Current and available funds

\- Recurring expenses

\- Pending payments

\- Essential spending

\- Confirmed income

\- Payment options

\- Financial information contained in messages

\- Information extracted from images



\### Core Approach



> \*\*Let the LLM understand. Let the algorithm decide.\*\*



The system deliberately separates language understanding from financial decision-making.



The LLM is used for tasks involving ambiguity and unstructured information:



\- Extracting financial amounts from images

\- Interpreting financial messages

\- Identifying changes to financial events

\- Generating the final explanation



The actual affordability calculations and financial decisions are handled deterministically.



\### Architecture



```text

User Request

&#x20;    │

&#x20;    ▼

Profile \& Financial Data

&#x20;    │

&#x20;    ▼

Ledger Reconstruction

&#x20;    │

&#x20;    ├──────────────► Image Understanding

&#x20;    │

&#x20;    └──────────────► Message Understanding

&#x20;                             │

&#x20;                             ▼

&#x20;                      Structured Effects

&#x20;                             │

&#x20;                             ▼

&#x20;                    Financial Forecast

&#x20;                             │

&#x20;                             ▼

&#x20;                   Affordability Engine

&#x20;                             │

&#x20;                             ▼

&#x20;                   Payment Plan Selection

&#x20;                             │

&#x20;                             ▼

&#x20;                      Validation

&#x20;                             │

&#x20;                             ▼

&#x20;                        Explanation

Key Components



Financial Ledger



Reconstructs the user's financial state from the available events and transactions.



Currency Normalization



Normalizes financial values using the relevant exchange-rate information.



Message \& Image Understanding



Uses an LLM to convert unstructured information into structured financial effects.



Forecasting



Projects future income and spending to determine how much can safely be paid and when.



Affordability Engine



Deterministically calculates the affordability status, safe payment amount, payment method, and earliest feasible payment date.



Payment Planning



Generates and validates possible payment plans against the financial forecast.



Validation \& Evaluation



The system includes extensive validation and evaluation to detect incorrect outputs, regressions, and unsafe decisions.



What I Learned



The main lesson from building the system was that using an LLM for every part of a financial decision is not necessarily the best approach.



A more reliable architecture is to use AI where interpretation is required and deterministic code where correctness matters.



AI handles ambiguity. Code handles certainty. Evaluation finds the gaps.



Results



🏆 2nd Place globally



HackerRank Orchestrate — September 2026



The competition solution and full implementation are kept private.



Tech Stack

Python

Large Language Models

Pandas

Deterministic financial calculations

Automated testing

Evaluation and regression testing

Repository



This repository is a public showcase of the project.



The complete competition implementation is maintained separately and is not included here.



Author



Shaurya Gupta

