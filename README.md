# **A/B Testing Campaign Analysis**

## **Project Overview**

This project involves the analysis of an A/B testing dataset related to marketing campaigns. The dataset compares two groups: one exposed to ads (`ad`) and another shown public service announcements (`psa`). The goal is to determine whether the ads significantly influenced user behavior and how much of the success can be attributed to the ads. 

The analysis answers the following key business questions:
- Would the campaign be successful?
- If the campaign was successful, how much of that success can be attributed to the ads?

## **Table of Contents**
1. [Project Structure](#project-structure)
2. [Dataset Information](#dataset-information)
3. [Installation & Requirements](#installation--requirements)
4. [Analysis Steps](#analysis-steps)
   - [Data Cleaning](#data-cleaning)
   - [Univariate Analysis](#univariate-analysis)
   - [Bivariate Analysis](#bivariate-analysis)
   - [A/B Testing](#ab-testing)
   - [Statistical Significance Testing](#statistical-significance-testing)
5. [Key Findings](#key-findings)
6. [Future Work](#future-work)
7. [Contributing](#contributing)
8. [License](#license)
9. [Contact](#contact)

## **Dataset Information**

The dataset contains information about users exposed to an A/B marketing campaign, where some users viewed advertisements and others saw public service announcements.

### **Data Dictionary**
- **Index**: Row index
- **user id**: Unique identifier for each user (removed for analysis)
- **test group**: `"ad"` for users who saw advertisements, `"psa"` for users shown public service announcements
- **converted**: `True` if the user bought the product, `False` otherwise
- **total ads**: The total number of ads seen by a person
- **most ads day**: The day when the person saw the most ads
- **most ads hour**: The hour of the day when the person saw the most ads

### **Data Statistics**
- **Total Rows**: 588,101
- **Columns**: 5 (post-cleaning)
- **Missing Values**: None

## **Installation & Requirements**

To run the analysis locally, ensure that the following dependencies are installed:

1. **Python 3.8+**
2. **Required Libraries**:
   - `numpy`
   - `pandas`
   - `matplotlib`
   - `seaborn`
   - `scipy`

## **Analysis Steps**

### **1. Data Cleaning**
   - Duplicate `user id` records were removed.
   - The `user id` column was dropped since it's not useful for analysis.
   - Unnecessary columns like `Unnamed: 0` were also removed.
   - Data types were validated, and no missing values were present.

### **2. Univariate Analysis**
   - **Test Group Distribution**: Visualized using pie and count plots to see the split between the experimental and control groups.
   - **Conversion Rates**: Identified the percentage of users who converted (made a purchase) after being exposed to the ads.
   - **Ad Exposure by Day and Hour**: Analyzed the most frequent days and times when users saw ads.

### **3. Bivariate Analysis**
   - Investigated relationships between the **test group** and conversion rate.
   - Evaluated conversion rates by **most ads day** and **most ads hour** using cross-tabulations and visualizations.
   - **Key Insights**: Ads had varying impacts based on the day and hour users were exposed to them.

### **4. A/B Testing**
   - Compared the conversion rates between the **ad** and **psa** groups.
   - Conversion rates for the ad group were higher, indicating the ads had a positive impact.

### **5. Statistical Significance Testing**
   - **Chi-Square Test**: Performed to check the significance of relationships between the test group and conversion.
   - **ANOVA**: Tested whether the number of ads seen differed significantly between groups.
   - **Results**: The Chi-Square test indicated a statistically significant difference in conversion rates between the ad and psa groups, confirming the ads' effectiveness.

---

## **Key Findings**

1. **Ads Significantly Boost Conversion**: Conversion rates for the ad group (2.55%) were higher than the control group (1.78%).
2. **Statistical Significance**: Chi-square and ANOVA tests confirmed that the difference between the test groups was statistically significant.
3. **Optimal Ad Timing**: Conversion rates were higher during the afternoon and evening hours (14:00 to 20:00).
4. **Days of Impact**: Users exposed to ads on Monday and Tuesday showed higher conversion rates compared to other days.

---

## **Future Work**
- **Time-Series Analysis**: Explore time-series modeling for ad exposure to identify optimal windows for future campaigns.
- **Personalization**: Investigate whether demographic or behavioral segmentation could yield more personalized and effective ad campaigns.
- **Machine Learning Model**: Develop a machine learning model to predict which users are more likely to convert based on exposure patterns.

---

## **Contributing**

We welcome contributions to improve this analysis. Please follow these steps to contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/new-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Open a Pull Request.

---

## **License**

This project is licensed under the MIT License - see the [Apache2.0](LICENSE) file for details.

---

## **Contact**

For any questions, feel free to reach out:

- **Name**: Rounak Pyne
- **Email**: rounakpyne.official@gamil.com

---
