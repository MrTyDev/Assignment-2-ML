SPAM DETECTION ALGORITHM COMPARISON
==============================
Name: Alexander Alfaro

This README provides instructions on how to execute the code for Assignment 2, which compares three supervised learning algorithms for spam detection on the Spambase dataset.

PREREQUISITES
------------
The following Python packages are required:
- numpy
- pandas
- scikit-learn
- matplotlib
- scipy
- tabulate
- seaborn

You can install these packages using pip:

pip install numpy pandas scikit-learn matplotlib scipy tabulate
```


FILES
-----
- Assignment_2.ipynb: The Jupyter notebook containing the analysis code
- spambase.data: The Spambase dataset from UCI repository
- README.txt: This file

EXECUTION INSTRUCTIONS
---------------------
1. Make sure all required packages are installed
2. Place the "spambase.data" file in the same directory as the notebook
3. Run the notebook using Jupyter:
   ```
   python spam_comparison.py
   ```

OUTPUT
------
The script will produce:
1. Console output showing:
   - Dataset information
   - Cross-validation results for each metric (accuracy, F1-score, training time)
   - Friedman test results
   - Nemenyi test results (if applicable)
   - Summary of all results

2. Generated images:
   - critical_difference_accuracy.png: Critical difference diagram for accuracy
   - critical_difference_f1.png: Critical difference diagram for F1 score
   - critical_difference_time.png: Critical difference diagram for training time
   - performance_comparison.png: Comparison of all metrics across folds

IMPLEMENTATION DETAILS
---------------------
- The script implements three supervised learning algorithms:
  1. Random Forest
  2. Support Vector Machine (SVM)
  3. K-Nearest Neighbors (KNN)
- Evaluation is done using stratified 10-fold cross-validation
- Statistical significance is determined using the Friedman test (α = 0.05)
- If significant differences are found, the Nemenyi post-hoc test is applied
- The critical difference (CD) is calculated at the 0.05 significance level

NOTE: The Friedman and Nemenyi tests are implemented from scratch as required by the assignment, without using any library functions that directly compute these tests. 