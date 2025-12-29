# Aircraft Turnaround Delay Risk & Impact Prediction

## Overview
Aircraft turnaround is the critical phase between an aircraft’s arrival
and its subsequent departure. Delays during this phase can cascade into
network-wide disruptions, increased operational costs, and passenger dissatisfaction.

This project demonstrates how machine learning can be used as a
**decision-support tool** to:
- Predict the risk of aircraft turnaround delays
- Estimate the potential delay duration

The focus is on **operational relevance, interpretability, and responsible use**
of machine learning rather than complex black-box models.

---

## Problem Statement
Airport operations involve tightly coupled processes such as gate allocation,
ground handling, refueling, cleaning, and crew coordination.

This project addresses two key operational questions:
1. *Is a given flight at risk of experiencing a turnaround delay?*
2. *If a delay occurs, how severe might it be?*

By separating risk prediction from impact estimation, the project mirrors
real-world operational decision-making workflows.

---

## Data Strategy
Due to the sensitive nature of real airport operational data,
a **synthetic dataset** is generated to simulate realistic turnaround scenarios.

The dataset includes:
- Arrival delay minutes
- Aircraft type (narrowbody / widebody)
- Gate availability
- Ground staff availability
- Weather conditions
- Time of day (peak / off-peak)
- Turnaround delay risk (binary)
- Turnaround delay duration (minutes)

Synthetic data generation allows explicit modeling of cause–effect relationships
while avoiding the use of proprietary or confidential information.

---

## Exploratory Data Analysis (EDA)
EDA focuses on identifying operational bottlenecks and compounding effects, such as:
- The relationship between arrival delays and turnaround delays
- The impact of gate constraints and staffing levels
- Differences in delay behavior during peak and off-peak periods

The analysis prioritizes **insight generation** over exhaustive visualization.

---

## Modeling Approach
Two simple and interpretable models are used:

- **Logistic Regression** for turnaround delay risk prediction
- **Linear Regression** for turnaround delay duration estimation

These models are intentionally selected to:
- Ensure transparency and explainability
- Support trust in operational environments
- Avoid black-box decision-making in safety-critical systems

---

## Evaluation
Model evaluation focuses on practical usefulness rather than maximum accuracy:
- Classification metrics and confusion matrix are used for risk prediction
- MAE and RMSE are used for delay duration estimation

In airport operations, missing a high-risk delay event is often more costly
than flagging a low-risk flight unnecessarily.

---

## Limitations & Ethical Considerations
- The dataset is synthetic and based on assumed operational relationships.
- Real-world airport environments involve additional constraints,
  uncertainty, and data quality challenges.
- Model outputs should not be used as the sole basis for operational decisions.

Machine learning is positioned as a **support tool for human decision-makers**,
not as an automated controller.

---

## Conclusion
This project illustrates a responsible application of machine learning
to aircraft turnaround operations.

By emphasizing operational context, interpretability, and limitations,
the project highlights how ML can support proactive and risk-aware
airport planning without replacing human expertise.

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
## Author
Sandesh Duduskar
