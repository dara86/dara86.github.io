# Data Science Portfolio
**Author:** Darragh Coyle
**Focus:** Statistical Inference and Data Visualization  
**Contact:** [LinkedIn](https://www.linkedin.com/in/darragh-coyle/) | [Your Email]


# Man vs. Keyboard: Statistical Analysis of Typing Ability

![Tools](https://img.shields.io/badge/Tools-R%20|)



## 📄 [Statistical Report (PDF)](./report.pdf)

## Summary
**Objective:** Collect data from day-to-day life and use statistics to gain deeper insights.

---

## 2. Data Collection (Originality)
* **Source:** Longitudinal study over 4 weeks ($N=30$ trials).
* **Tools:** TypingTest.com (Data Generation), Excel/CSV (Data Entry).
* **Variables:**
    * **Performance:** WPM (Words Per Minute), Accuracy (%).
    * **Environment:** Caffeine (Y/N), Music (Y/N), Time of Day, Location (Public/Private).

---

## 3. Methodology (Rigor)
This analysis moves beyond simple descriptive statistics (averages) to inferential statistical modeling.

| Question | Statistical Test | Justification |
| :--- | :--- | :--- |
| **Does practice predict speed?** | `Linear Regression` | Modeled the learning curve to quantify exact WPM gain per trial. |
| **Does music help focus?** | `Bayesian Inference` | Updated prior beliefs ($P=0.5$) with observed data to calculate posterior probability. |
| **Do I work better in public?** | `Fisher's Exact Test` | Used due to small sample sizes in the contingency table to test independence. |

---

## 4. Key Findings & Actionable Insights
### 📉 The "Mozart Effect" is Negative
Using Bayes' Theorem, I calculated the posterior probability of a successful run (WPM > Median) given music was playing:
* **Prior Belief:** 50% chance of success.
* **Posterior Probability:** **41.7%** chance of success.
* **Action:** Deep work sessions requiring high precision should be done in silence.

### 📉 Practice $\neq$ Improvement
* **Result:** Linear regression showed a significant positive trend ($p=0.039$), but the $R^2$ was only **0.113**.
* **Interpretation:** Repetition explains only 11% of the variance. 89% of improvement is likely driven by **technique correction** (ergonomics) rather than volume of practice.

### 🏠 The "Public Workspace" Fallacy
* **Result:** I am statistically more likely to work in public during the day ($OR=0.167$).
* **Constraint:** This was identified as a confounding variable—libraries are closed at night, forcing private work, rather than a behavioral preference.

---

## Visualizations
*(See full report for detailed R-generated plots)*

*Figure 1: Bayesian update showing the shift in probability when music is introduced.*
