# ML-Project-Checklist
This checklist can guide you through your Machine Learning projects. 

There are eight main steps:

1. Frame the problem and look at the big picture.
2. Get the data.
3. Explore the data to gain insights.
4. Prepare the data to better expose the underlying data patterns to Machine Learning algorithms.
5. Explore many different models and short-list the best ones.
6. Fine-tune your models and combine them into the best ones.
7. Present your solution.
8. Launch, monitor and maintain your system.


### Frame the problem and Look at the Big Picture

1. Define the objective in business terms.
2. How will your solution be used?
3. What are the current solutions/workarounds (if any)?
4. How should you frame this problem (supervised/unsupervised, online/offline, etc.)?
5. How should performance be measured?
6. Is the performance measure aligned with the business objective?
7. What would be the minimum performance needed to reach the business objective?
8. What are comparable problems? Can you reuse experience or tools?
9. Is human expertise available?
10. How would you solve the problem manually?
11. List the assumptions you (or others) have mane so far.
12. Verify the assumptions if possible.


### Get the Data
**Note: Automate as much as possible so you can easily get fresh data.**

1. List the data you need and how much you need.
2. Find and document where you can get the data.
3. Check how much space it will take.
4. Check legal obligations, and get authorization if necessary.
5. Get access authorizations.
6. Create a workspace (with enough storage space).
7. Get the data.
8. Convert the data to a format you can easily manipulate (without changing the data itself).
9. Ensure sensitive information is deleted and protected (e.g., anonymized).
10. Check the size and type of data (time series, sample, geographical, etc.).
11. Sample a test set, pull it aside and never look at it (no data snooping!).


### Explore the Data

**Note: Try to get insights from a field expert for these steps.**

1. Create a copy of the data for exploration (sampling it down to a manageable size if necessary).
2. Create a jupyter notebook to keep a record of your data exploration.
3. Study each attribute and its characteristics:
    - Name
    - Type (categorical, int/float, bounded/unbounded, text, structured, etc.)
    - % of missing values
    - Noisiness and type of noise (stochastic, outliers, rounding errors, etc.)
    - Possibly useful for the task?
    - Type of distribution (Gaussian, uniform, logarithmic, etc.)
4. For supervised learning tasks, identify the target attribute(s).
5. Visualize the data.
6. Study the correlations between attributes.
7. Study how you would solve the problem manually.
9. Identify the promising transformations you may want to apply.
10. Document what you have learned.

### Prepare the Data

Notes:

- Work on copies of the data (keep the original dataset intact).
- Write functions for all the data transformations you apply, for five reasons:
  * So you can easily prepare the data the next time you get a fresh dataset
  * So you can apply these transformations in future projects
  * To clean and prepare the test set
  * To clean and prepare new data instances once your solution is live
  * To make it easy to treat your preparation choices as hyperparameters
  

1. Data Cleaning:
  * Fix or remove outliers (optional).
  * Fill in missing values (e.g., with zero, mean, median...) or drop their rows (or columns)
2. Feature selection (optional):
  * Drop the attributes that provide no useful information for the task.
3. Feature engineering, where appropriate:
  * Discretize continuous features.
  * Decompose features (e.g., categorical, date/time, etc.).
  * Add promising transformations of features (e.g., log(x), sqrt(x), x^2, etc.).
  * Aggregate features into promising new features.
4. Feature scaling: standardize or normalize features.
