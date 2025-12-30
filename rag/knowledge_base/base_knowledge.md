# Knowledge Base for Robo-Advisor Explanations

This document contains the core reference material used by the explanation engine. 
It provides simple definitions and short explanations that help generate clear and 
transparent answers for users. All content is educational and does not represent 
financial advice.

---

## 1. Risk Profiles

### Conservative Risk Profile
A conservative investor prefers stability and low risk. They accept smaller returns 
in exchange for less volatility. Their main goal is to protect their capital. 
Portfolios for conservative investors typically include a high share of bonds and 
other lower-risk assets.

### Moderate Risk Profile
A moderate investor accepts some risk in order to achieve balanced growth. They can 
handle short-term fluctuations but still prefer a controlled level of risk. Their 
portfolio usually mixes both equities and bonds in a balanced way.

### Aggressive Risk Profile
An aggressive investor is comfortable with market fluctuations and higher volatility. 
Their main goal is strong long-term growth. Portfolios for aggressive investors 
usually contain a large share of equities and only a small share of stable assets.

---

## 2. Key Questionnaire Concepts

### Risk Preference
Risk preference describes how comfortable someone is with financial uncertainty. 
Higher risk preference normally increases the chance of being classified as 
moderate or aggressive.

### Investment Horizon
Investment horizon is the number of years a person expects to stay invested. 
A longer horizon allows more time for markets to recover from short-term losses. 
Long horizons often support a higher risk profile.

### Loss Aversion
Loss aversion shows how strongly a person dislikes losing money. High loss aversion 
reduces the willingness to take risk. It often leads to a conservative or moderate 
classification.

### Financial Knowledge
This refers to how well someone understands investment concepts. Higher financial 
knowledge usually increases confidence in handling risk and can support a moderate 
or aggressive profile.

### Investment Experience
Experience measures previous exposure to investing. Someone who has invested before 
may be more comfortable with fluctuations. More experience often leads to a slightly 
higher risk tolerance.

### Income Band
Income helps determine financial stability. Higher income can reduce pressure on 
savings and may support a higher risk profile. Lower income usually leads to more 
cautious behaviour.

### Primary Investment Goal
People invest for different reasons. Common goals include:

- Capital preservation  
- Balanced growth  
- Aggressive long-term growth  

The goal strongly influences risk. Someone focused on preservation usually prefers 
conservative portfolios, while long-term growth goals may support higher risk.

---

## 3. Modern Portfolio Theory (MPT)

Modern Portfolio Theory explains how to build a portfolio that balances risk and 
return. The idea is that combining different assets reduces risk because they do 
not move in the same direction at the same time.

MPT introduces concepts such as diversification and the efficient frontier. 
In this project, MPT is used in a simple way to create allocations that match the 
investor’s predicted risk profile. This use is educational and does not represent 
real portfolio management.

---

## 4. SHAP and Explainability

SHAP values show how each feature contributed to the model’s prediction. A positive 
SHAP value means the feature pushed the prediction toward a specific class, while a 
negative value means it reduced the probability for that class.

Examples:
- Higher financial knowledge may push toward the aggressive class.
- High loss aversion may push toward the conservative class.
- Older age may push toward a lower risk class.
- Longer horizon may support higher risk.

SHAP helps users understand why the model made a specific prediction.

---

## 5. Regulation and Ethical Context

### MiFID II
MiFID II requires investment recommendations to match a client’s objectives and 
risk profile. It also requires clear explanations that users can understand.

### EU AI Act
AI systems in finance should be transparent, fair, and trustworthy. Explanations 
must be easy to understand and should avoid misleading users.

### Ethical Position of This Project
This system is a technical prototype for educational use. It does not make real 
recommendations, and it does not replace professional advice.

---

## 6. Disclaimer Text

### Full Disclaimer
This system is a technical prototype created for academic purposes. It does not 
provide financial advice, investment recommendations, or personalised financial 
planning. All explanations are simplified and should not be used for making 
real investment decisions.

### Short Disclaimer (for final RAG output)
This explanation is for educational purposes only and is not financial advice.

---

## 7. Mini Explanations and FAQ

### Why was I classified as Aggressive?
A person is classified as aggressive when their questionnaire answers show a higher 
comfort with volatility, longer investment horizons, stronger financial knowledge, 
or a growth-focused goal. Features that reduce loss sensitivity or show experience 
can also support this result.

### Why is investment horizon important?
A longer horizon gives more time to recover from market downturns. This often allows 
a slightly higher level of risk.

### Why does loss aversion matter?
People who strongly dislike losses tend to avoid high-risk investments. High loss 
aversion usually pushes the model towards a conservative or moderate profile.

### What does Moderate risk mean?
Moderate risk means a balance between stability and growth. The investor accepts 
some fluctuations but still prefers controlled risk.
