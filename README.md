# Man vs. Keyboard: Statistical Analysis of Human Performance

**Author:** [Your Name]  
**Date:** December 2025  
**Tools:** R, Linear Regression, Bayesian Inference, Hypothesis Testing

## 📄 [Download Full Statistical Report (PDF)](./Statistics_Porfolio.pdf)

---

## Project Overview
[cite_start]This project applies frequentist and Bayesian statistical methods to analyze the learning curve of typing speed and accuracy over a 4-week longitudinal study ($N=30$)[cite: 18]. The study investigates the impact of environmental variables (caffeine, audio stimuli, location) on motor performance, challenging common assumptions about self-improvement and the "practice makes perfect" adage.

## Key Statistical Findings

### 1. The "Practice" Myth (Linear Regression)
* **Hypothesis:** $H_1: \beta_1 \neq 0$ (Speed changes significantly over time).
* [cite_start]**Result:** While a statistically significant positive trend was observed ($p=0.038$), the model yielded a low Adjusted $R^2$ of **0.113**[cite: 183, 190].
* **Inference:** Simple repetition explains only **11.3%** of the variance in speed improvement. [cite_start]The remaining 88.7% is likely attributed to latent variables such as ergonomic technique corrections (e.g., stabilizing hand placement) rather than raw repetition[cite: 194].

### 2. The "Mozart Effect" Debunked (Bayesian Inference)
* [cite_start]**Method:** Utilized Bayes' Theorem to update the prior belief ($P(H)=0.5$) that music improves focus[cite: 457].
* [cite_start]**Result:** The posterior probability $P(H|D)$ dropped to **41.7%**[cite: 504].
* [cite_start]**Inference:** Contrary to the prior belief, the evidence suggests that audio stimuli act as a performance inhibitor, reducing the probability of a "High WPM" run by **8.3%**[cite: 504].

### 3. Environmental Impact (Fisher's Exact Test)
* **Method:** Analyzed the association between Location (Public vs. Private) and Time of Day.
* [cite_start]**Result:** A significant association was found ($OR=0.167$, $p=0.049$)[cite: 418, 429].
* [cite_start]**Inference:** While the data suggests a strict separation of work environments, qualitative analysis reveals this is confounded by the operating hours of public spaces (libraries/cafés) rather than purely disciplined choice[cite: 432].

---

## 💻 R Code Snippets
Below are the core statistical models used in the analysis.

### Linear Regression Model
Determining if trial number predicts WPM score.
```r
# Linear Model: WPM as a function of Trial Number
lm_speed <- lm(wpm ~ trial, data = df)
summary(lm_speed)

# Result: p-value = 0.03875, Adj R-squared = 0.1132
