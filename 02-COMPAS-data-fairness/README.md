# COMPAS Data Fairness Analysis

## Overview

This exercise investigates the challenges and trade-offs of applying machine learning models fairly in high-stakes domains—specifically, recidivism prediction using the widely studied COMPAS dataset. The primary goal is to implement, evaluate, and critically analyze how various fairness definitions affect the assessment of a logistic regression risk model for criminal justice and to reflect on the social and ethical stakes involved.

## Tools & Data

- **Python 3.x**
- **Jupyter/Colab Notebooks**
- **Libraries:** pandas, matplotlib, seaborn, scikit-learn
- **Dataset:** COMPAS dataset (Florida, 2013-2014) as described in `Compas-Data-Description.pdf`
- **Fairness concepts:** As outlined in `Fairness-Definitions-Explained.pdf`

## Project Objective

**Key Questions:**
- How fair is a standard (logistic regression) classifier when predicting two-year recidivism on real-world data?
- How does the choice of fairness definition (group vs. conditional, error rate-based vs. calibration, etc.) affect our assessment?
- What complexities and limitations arise when operationalizing fairness in practice?

**Task:**  
Build, evaluate, and analyze a predictive model for recidivism using COMPAS data. Apply multiple fairness definitions per academic best practice. Critically discuss the impact of each and synthesize implications for policymakers and practitioners.

## Exercise Structure & Methods

### 1. Background & Required Readings

- **COMPAS Dataset Description:** Essential for understanding variables, context, and stakes.
- **Fairness Definitions Explained:** Provides a taxonomy of statistical, individual, and causal fairness, which are applied directly to the modeling outputs.

### 2. Implementation Workflow

- **Data Loading & EDA:** Import dataset, inspect key variables (e.g., sex, race, priors, two_year_recid), and examine distributions and missingness.
- **Model Training:** Implement logistic regression for binary recidivism prediction, using appropriate features.
- **Performance Assessment:** Evaluate ROC AUC, confusion matrices, and other accuracy measures.
- **Fairness Assessment:** Compute and interpret various fairness metrics, including:
    - Statistical Parity/Group Fairness
    - Conditional Statistical Parity
    - Predictive Parity
    - Error Rate Balances (False Positive/Negative Rate)
    - Equal Opportunity, Equalized Odds
    - Calibration/Test-Fairness
    - Individual-level (causal, counterfactual) fairness indicators
- **Visualization:** Use charts and confusion matrices to illustrate key findings.
- **Synthesis:** Write up analysis, discussing where definitions agree or conflict, and reflect on real-world impact.

## Evaluation Criteria

- **Technical accuracy:** Correct application of modeling and metrics.
- **Fairness nuance:** Coverage of trade-offs, incompatibilities among fairness measures (as per Verma & Rubin).
- **Ethical reflection:** Ability to relate metric results to actual social outcomes and policy decisions.
- **Clarity:** High-quality notebook code and clear, well-commented output.

## How to Run

1. Install required Python packages.
2. Open `BA840-Team-08-COMPAS-Data-Fairness.ipynb` in Jupyter or Google Colab.
3. Run cells sequentially to:
    - Load and inspect COMPAS data.
    - Train the ML model and generate predictions.
    - Calculate accuracy and fairness metrics.
    - Visualize results for group comparison.
    - Read and interpret conclusions.
4. Use the PDF guides for additional background/context.

## Requirements

- Python ≥ 3.7, with packages: pandas, scikit-learn, matplotlib, seaborn
- No external data downloads required—the dataset is loaded as part of the workflow.

## Learning & Takeaways

- Learned the complexity and necessity of multiple fairness definitions in high-impact ML tasks.
- Practiced recidivism prediction but went beyond simple accuracy to critically evaluate real-world implications.
- Developed cross-cutting analytical skills—connecting technical metrics with ethical and policy dimensions.

## Project Details

- **Completed:** August 2025  
- **Course:** Responsible AI & Data Ethics (BA840), Boston University MSBA  
- **Team Contributors:**  
  - Gunjan Sharma  
  - Jasmine Gohil  
  - Jenil Shah  
  - Saachi Dholakia  
  - Sneha Ekka

*This project demonstrates the critical role of a nuanced fairness analysis in deploying real-world, high-stakes ML systems and serves as a template for conducting balanced ethical evaluations of algorithmic tools in justice, finance, and other sensitive settings.*
