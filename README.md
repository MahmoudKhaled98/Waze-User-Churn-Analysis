# Waze User Churn Analysis

Phase 1: I aim to investigate user churn within the Waze app by analyzing user behavior and characteristics from a dataset of 14,999 records. This analysis focuses on identifying patterns that influence user retention and informing strategies to enhance engagement and reduce churn rates. The project involves exploratory data analysis (EDA), data cleaning, and assessing user behavior to provide insights for refining Waze's retention strategies.

Phase 2: Currently, I am in the early stages of the project, having completed a proposal and utilized Python to inspect and organize the dataset. This phase continues the focus on identifying patterns influencing user retention through EDA and data cleaning.

Phase 3: The next step is to apply statistical methods to analyze the data. I will determine if there is a statistically significant difference in the mean number of rides between iPhone and Android users, as requested by my project manager, Sylvester Esperanza. This involves a two-sample hypothesis test (t-test) based on ride data segmented by device type.


## Table of Contents
- [Introduction](#introduction)
- [Phase I: EDA on Waze User Churn Data Phase-I](#phase-i-eda-on-waze-user-churn-data-phase-i)

  - Task 1: Imports
  - Task 2: Data Exploration, Cleaning, and Preparation
  - Task 3: Key Insights


- [Phase II: EDA on Waze User Churn Data Phase-II](#phase-ii-eda-on-waze-user-churn-data-phase-ii)

  - Task 1: Imports, Links, and Loading
  - Task 2: Data Exploration, Data Cleaning, and Preparation
  - Task 3: Building Visualizations
  - Task 4: Evaluating and Sharing Results

- [Phase III: Hypothesis Testing Analysis on Waze User Churn Data Phase-I](#phase-iii-hypothesis-testing-analysis-on-waze-user-churn-data)
 
    - Task 1: Imports and Data Loading
	- Task 2: Data Exploration and Analysis
    - Task 3: Hypothesis Testing
    
- [Conclusion](#conclusion)
- [Summary for Stakeholders](#summary-for-stakeholders)
- [Executive Summaries Documentations](#executive-summaries-documentations)

## Introduction

The goal of this analysis is to uncover factors that influence user churn within the Waze app through exploratory data analysis (EDA). By understanding these drivers, Waze can implement targeted strategies to improve user retention. The project is structured into three main tasks: understanding the context, data, and variables.
In the first phase, the analysis focuses on identifying the key factors influencing user churn. The second phase continues to explore these drivers and includes data visualizations to effectively communicate insights. Finally, the last phase aims to determine whether there is a statistically significant difference in the mean number of rides between iPhone and Android users. Understanding this difference will enable Waze to better tailor its strategies for enhancing user retention.


## Phase I: EDA on Waze User Churn Data Phase-I

### Task 1: Imports and Data Loading

#### Importing Packages
To begin, we will import several essential Python libraries:
- `numpy` for numerical operations
- `pandas` for data manipulation
- `matplotlib.pyplot` for visualizations
- `seaborn` for enhanced visualizations

---

### Task 2: Data Exploration, Cleaning, and Preparation

#### Loading the Dataset
- The dataset is loaded into a pandas DataFrame for exploration.

#### Summary Information
- **Data Types**: The dataset includes 3 `float64`, 8 `int64`, and 2 `object` data types, totaling 12 columns and 14,999 rows.
- **Missing Values**: The `label` column contains 700 missing values.

#### Null Values and Summary Statistics
- **Overall Patterns**: Mean values are similar for users with and without churn labels.
- **Key Insights**: Differences in minimum values for metrics suggest potential bias in missing data, possibly related to early users.
- **Churn vs. Retained Users**: Churned users averaged about 3 more drives in the last month, while retained users used the app on more than twice as many days.

#### Comparative Analysis
- **Driving Distances**: Median churned users drove around 698 kilometers daily on driving days—240% more than retained users.
- **Driving Duration**: Churned users spent about 2.5 additional hours driving.
- **Usage Patterns**: Churned users exhibited more intensive but less frequent usage, averaging about 3 more drives in the last month.

---

### Task 3: Key Insights

#### User Retention Overview
- **Retention Rate**: 82% of users are retained, while 18% have churned, underscoring the importance of targeted retention strategies.

#### Driving Behavior Patterns
- **Distinct Usage Profiles**: Churned users drove farther and longer in fewer days, suggesting unique user profiles worth exploring further.

#### User Demographics
- **Device Usage**: Android users represent 36% of the sample, while iPhone users make up 64%, highlighting opportunities for tailored marketing strategies.

#### Churn Rate Analysis
- **Device Influence on Retention**: Churn rates between iPhone and Android users differ by only 1 percentage point, indicating that device type does not significantly affect retention.

#### Implications of Driving Behavior
- **User Needs**: Users in this dataset drive extensively, possibly including long-haul drivers, suggesting a need to address their specific requirements, which may differ from casual drivers.

 [Executive Summary](https://docs.google.com/presentation/d/12WrMK0GGLcDfY8RrOpu5qq8GxgBxJsmBDJT_bjpUJ7o/edit?usp=sharing)

---



## Phase II: EDA on Waze User Churn Data Phase-II

### Task 1: Imports, Links, and Loading

- **Imports**: Import essential Python libraries, including `pandas`, `numpy`, and `matplotlib` for data manipulation and visualization.
- **Loading Data**: Store the dataset as a DataFrame object named `df`.

---

### Task 2: Data Exploration, Cleaning, and Preparation

- **Data Overview**: Analyze the structure and summary statistics of the dataset.
- **Handling Missing Values**: Check for missing data, particularly in the label column, and determine an appropriate strategy to handle it.
- **Outlier Detection**: Identify and manage outliers in key metrics such as `sessions`, `drives`, and `duration_minutes_drives`.

---

### Task 3: Building Visualizations

- **Types of Visualizations**: Create various charts to explore the spread and distribution of important variables, including box plots, histograms, and scatter plots.
- **Key Variables**: Focus on variables like `sessions`, `drives`, and user demographics to visualize user engagement and churn rates.

---

### Task 4: Evaluating and Sharing Results

- **Summary of Findings**: Compile insights from the visualizations to provide recommendations for reducing churn and enhancing user retention.

- [Tableau Visualization](https://public.tableau.com/app/profile/mahmoud.hanafy4551/viz/WazeappUserchurnproject/UserChurnProjectWazeApplication)

- [Executive Summary](https://docs.google.com/presentation/d/1ns16hP8cN935IBsRbXzjd1eCSNo3vzRv2M91CuwY2bI/edit#slide=id.g2467ac73dde_0_430)


## Phase III: Hypothesis Testing Analysis on Waze User Churn Data

### Task 1: Imports and Data Loading

#### Importing Packages
To begin, several key Python libraries will be imported:
- **numpy** for numerical operations
- **pandas** for data manipulation
- **scipy.stats** for statistical tests

#### Loading the Dataset
The dataset will be loaded into a pandas DataFrame to facilitate further exploration.

---

### Task 2: Data Exploration and Analysis

#### Descriptive Statistics
Descriptive statistics will provide a summary of the data, helping identify outliers, patterns, and trends within the dataset.

#### Relationship Between Device Type and Drives
The dataset includes a categorical variable, **device**, labeled as *iPhone* and *Android*. To enable analysis, these labels will be converted into integers.

#### Average Number of Drives
The relationship between device type and the number of drives will be explored by calculating the average number of drives for each device type. Initial findings indicate that iPhone users have a higher average number of drives, though further analysis is necessary to determine if this difference is statistically significant.

---

### Task 3: Hypothesis Testing

#### Research Question
Is there a statistically significant difference in the mean number of drives between iPhone users and Android users?

#### Steps for Hypothesis Testing
1. **State the null hypothesis** ($H_0$): There is no difference in the average number of drives between iPhone and Android users.
2. **State the alternative hypothesis** ($H_A$): There is a difference in the average number of drives between iPhone and Android users.
3. **Choose a significance level** (`0.05`).
4. **Compute the p-value** using a two-sample t-test.

#### Performing the t-test
The t-test will be conducted using the `stats.ttest_ind()` function. The **drives** column will be isolated for both iPhone and Android users, and the t-test will be applied to determine if the observed differences are statistically significant.

#### Findings:

The analysis revealed a `p-value of 0.143351`, which is greater than the significance level of `0.05`. Therefore, I fail to reject the null hypothesis and conclude that the difference in the mean number of drives between iPhone and Android users is likely due to chance or sampling variance.

- [Executive Summary](https://docs.google.com/presentation/d/1JzgJGTucyfeozozWs4EcyzXp4TGfxXlcVz4ReGcuAc4/edit?usp=sharing)

## Conclusion
This analysis aimed to uncover factors influencing user churn within the Waze app through exploratory data analysis (EDA) and to assess differences in user behavior between iPhone and Android users. The findings revealed a churn rate of approximately `17%`, consistent across both device types. The analysis yielded a `p-value` of `0.143351`, which is greater than the `significance level of 0.05`. Thus, we fail to reject the null hypothesis, concluding that the difference in the mean number of drives between iPhone and Android users is likely due to chance or sampling variance.


### Key Insights 
- **Understanding user behavior** is essential for improving retention rates.
- The dataset indicates **potential bias due to missing values**, emphasizing the need for further investigation.
- **Distinct usage patterns** among churned users suggest opportunities for targeted user engagement strategies.
- **Users who drive longer distances** on driving days are more likely to churn, while those who drive more frequently are less likely to churn, presenting a contradiction worth exploring further.
- The analysis revealed an **overall churn rate of approximately `17%`**, with no significant differences between iPhone and Android users.
- A notable spike in app usage among users in the past month prompts the idea of reaching out to the Waze data team for insights into this increase.
- **Key observations from the EDA** included:
   - **Missing values** in the user churn label, necessitating further data processing before deeper analysis.
   - Numerous **outlying observations for driving distances** suggest the need for variable transformation to stabilize variation.
   - The **number of drives and sessions are strongly correlated**, potentially leading to redundant information if both are included in a model.
   - On average, **retained users have fewer drives than churned users**, raising further questions.
- **Future research** may explore additional factors influencing driving behavior and further hypothesis tests to understand user engagement better.

## Summary for Stakeholders
This analysis provides crucial insights into user behavior, retention rates, and data characteristics. With less than `18%` of users churning and approximately `82%` retained, understanding the reasons behind the recent spike in app usage is vital. **Key questions** that require addressing include:
- How does the **missing data in the user churn label** occur?
- Who are the **users with extremely high numbers of drives**? Are they rideshare or commercial drivers?
- Why do **retained users have fewer drives than churned users**? Could it be that churned users have a longer history with the Waze app?
- What are the **user demographics for retained versus churned users**?

In terms of variable distributions, nearly all were either **right-skewed or uniformly distributed**. The right-skewed distributions indicate that most users had values in the lower range, while uniform distributions suggest equal likelihood across the value range. While most data appeared valid, a few **outliers**, particularly in driving distances, raised concerns regarding discrepancies in maximum values for certain monthly variables.

Moving forward, it will be crucial to confirm with the Waze data team whether the **monthly variables were collected concurrently**, and to investigate the factors that may have triggered the recent surge in app usage. Overall, this analysis serves as a foundation for Waze to develop strategies to improve user retention and better meet the needs of its diverse user base. The conclusion of the **hypothesis test** suggests that no significant difference exists in the mean number of drives between device users, indicating that **retention strategies can be uniformly applied across platforms**.

## Executive Summaries Documentations

* [EDA on Waze User Churn Data Phase-I Executive Summary](https://docs.google.com/presentation/d/12WrMK0GGLcDfY8RrOpu5qq8GxgBxJsmBDJT_bjpUJ7o/edit?usp=sharing)
* [EDA on Waze User Churn Data Phase-II Executive Summary](https://docs.google.com/presentation/d/1ns16hP8cN935IBsRbXzjd1eCSNo3vzRv2M91CuwY2bI/edit#slide=id.g2467ac73dde_0_430)
* [Hypothesis Testing Analysis on Waze User Churn Data Executivetive Summary](https://docs.google.com/presentation/d/1JzgJGTucyfeozozWs4EcyzXp4TGfxXlcVz4ReGcuAc4/edit?usp=sharing)

## How to Run
1. **Clone the repository**:

    ```bash
    git clone <https://github.com/MahmoudKhaled98/Waze-User-Churn-Analysis.git>
    ```

2. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
3. **Run the notebook**:
    ```bash
    jupyter notebook
    ```

## References

 [pandas 2.0.3 Documentation](https://pandas.pydata.org/pandas-docs/version/2.0.3/)
 
 [NumPy 1.24.3 Documentation](https://numpy.org/doc/1.24/)
 
 [Matplotlib 3.7.1 Documentation](https://matplotlib.org/stable/contents.html)
 
 [Seaborn 0.12.2 Documentation](https://seaborn.pydata.org/whatsnew/v0.12.2.html)
 
 [SciPy 1.10.1 Documentation](https://docs.scipy.org/doc/scipy-1.10.1/)


