## Causal Inference with EconML: Analyzing Minimum Wage Effects on Unemployment

This repository investigates the potential impact of minimum wage (Mw.csv) changes on unemployment rates (unemployement.csv) in the United States using EconML's causal inference tools. 

**Key functionalities:**

* **Data Cleaning and Preprocessing:**
    * Loads unemployment and minimum wage data from CSV files.
    * Handles missing values using appropriate techniques like mode imputation.
    * Merges datasets based on State and Year.
    * Creates new features like Minimum Wage Change and Minimum Wage Treatment indicator.
* **Feature Engineering:**
    * Selects relevant features for analysis (e.g., Minimum Wage Change, CPI Average) and the target variable (Unemployment Rate).
    * Splits data into training and testing sets for model evaluation.
* **EconML for Causal Inference:**
    * **Average Treatment Effect (ATE):**
        * Estimates the overall average change in unemployment rates if the minimum wage increased for everyone.
        * Uses DoubleML, a two-stage econometric machine learning method for ATE estimation.
    * **Conditional Average Treatment Effect (CATE):**
        * Analyzes how the effect of minimum wage changes varies across states based on features like Minimum Wage Change and CPI Average.
        * Employs OrthoForest, a tree-based method for estimating heterogeneous treatment effects.

**Running the Script:**

1. Install required libraries (`pandas`, `numpy`, `scikit-learn`, `econml`, `torch`, etc.) using `pip install <library_name>`.
2. Place your unemployment and minimum wage data in CSV files named `unemployment.csv` and `Mw.csv` respectively, in the same directory as the script.
3. Run the script: `python causal_inference_min_wage.py`.

**Outputs:**

* The script prints the estimated Average Treatment Effect (ATE) and Conditional Average Treatment Effects (CATE) for minimum wage changes on unemployment rates.
* You can further analyze the results to understand the overall impact and potential variations in treatment effects across different states.

**Dependencies:**

* Python 3.x
* pandas
* numpy
* scikit-learn
* econml
* torch
* matplotlib

**Further Exploration:**

* Experiment with different EconML estimators for causal inference (e.g., CausalML, DRlearner).
* Explore alternative feature engineering techniques to potentially improve model performance.
* Visualize CATE results to gain insights into group-specific effects.

This code provides a starting point for analyzing causal relationships using EconML. Feel free to adapt and extend it for your specific research questions.
