# Research Project with Multiple and Logistic Regression

This research project processes large volumes of data obtained from the Colombian Institute for the Evaluation of Education (ICFES) to create a training model that predicts the global score and analyzes whether various socio-economic factors influence the score.

## Project Objective

The main objective of this project is to predict the *global score* (PUNTAJE GLOBAL) of students in the Saber Pro Test, a standardized assessment of higher education quality in Colombia. This prediction can be useful for identifying factors that influence student performance and helping educational institutions improve the quality of education.

## Context and Scope of the Project

- **Client:** Educational institutions, students, and government agencies.
- **Purpose:** To assist in potentially improving students' academic performance and optimizing educational resources.
- **End Users:** Educational institution administrators, students, teachers, and policymakers.

## Specific Objectives

1. **Identify Determinant Factors:** Determine which variables (e.g., socio-economic characteristics, educational background, etc.) have the most impact on the global score.
2. **Develop a Predictive Model:** Create a machine learning model that can predict students' global scores based on the provided data.
3. **Model Validation and Evaluation:** Evaluate the accuracy and robustness of the predictive model.
4. **Implementation of Strategies:** Propose strategies based on the model's findings to improve student outcomes.

## Success Criteria

- **Model Accuracy:** Achieve high accuracy in predicting the global score (e.g., low RMSE).
- **Interpretability:** The model should be interpretable to clearly identify the factors affecting the global score.
- **Applicability:** The model should be applicable in different contexts and regions, providing practical recommendations to improve student performance.
- **Impact on Educational Policies:** Use the findings to influence educational policies and teaching strategies.

## Situation Assessment

- **Available Resources:** Database of 548,962 rows and 66 columns, data analysis tools (Python), and expertise in machine learning and statistics.
- **Constraints:** Data quality, possible missing data, and variability in data from different institutions.
- **Assumptions:** The data provided is representative and of sufficient quality for analysis.

## Key Variables Definition

- **Target Variable:** PUNT_GLOBAL (students' global score).
- **Predictor Variables:** Other columns in the database, such as demographic, socio-economic, and academic characteristics.

## Risk Analysis and Mitigation

- **Data Risks:** Incomplete or inaccurate data. Mitigation: Data cleaning and handling missing values.
- **Technical Risks:** Difficulty in selecting and tuning the appropriate model. Mitigation: Testing multiple algorithms and cross-validation techniques.
- **Implementation Risks:** Resistance to change in educational institutions. Mitigation: Effective communication of the model's benefits and proper training for end-users.

## Project Planning

1. **Data Understanding:** Data exploration and cleaning.
2. **Data Preparation:** Data transformation and feature selection.
3. **Modeling:** Testing various machine learning algorithms.
4. **Model Evaluation:** Validation and tuning of the model.
5. **Deployment:** Implementing the model in a real environment.
6. **Monitoring and Maintenance:** Tracking the model's performance and making adjustments as necessary.

## Business Understanding

### Context

The Saber Pro Tests are a set of standardized assessments conducted in Colombia for students finishing their higher education studies. These tests are mandatory and serve as an indicator of the quality of higher education, as well as the level of competencies achieved by students. The results are used by educational institutions, employers, and educational authorities to assess academic performance and the quality of educational programs.

### Project Goal

This project aims to predict whether a student who took the Saber Pro Tests has received a scholarship for their university tuition. The target variable (`target`) is `ESTU_PAGOMATRICULABECA_Si`, indicating whether the student received a scholarship. This prediction can help identify factors associated with obtaining scholarships and design strategies to promote equity and access to higher education.

### Importance of Prediction

1. **Educational Policies:** Helps institutions and the government identify factors influencing scholarship attainment and design policies to promote equity in higher education access.
2. **Program Improvement:** Allows universities and other educational institutions to adjust their programs and support services to maximize scholarship opportunities for their students.
3. **Student Guidance:** Provides students and their families with valuable information on factors that could increase their chances of receiving a scholarship.

### Data Description

The data used in this project came from the Saber Pro Tests and contained various characteristics related to students and their test results. Key features include:

- **Personal and Demographic Data:**
  - `ESTU_TIPODOCUMENTO`: Type of identification document.
  - `ESTU_GENERO`: Student's gender.
  - `ESTU_FECHANACIMIENTO`: Student's date of birth.
  - `ESTU_DEPTO_RESIDE`: Department of Residence.
  - `ESTU_MCPIO_RESIDE`: Municipality of residence.
  - `ESTU_AREARESIDE`: Area of residence (urban or rural).

- **Academic and Financial Data:**
  - `ESTU_VALORMATRICULAUNIVERSIDAD`: University tuition value.
  - `ESTU_PAGOMATRICULABECA`: Indicator if the student received a scholarship.
  - `ESTU_PAGOMATRICULACREDITO`: This indicator indicates if the student paid tuition with credit.

- **Test Results:**
  - `MOD_INGLES_DESEM`, `MOD_INGLES_PNAL`, `MOD_INGLES_PNBC`: Performance in English tests.
  - `MOD_COMUNI_ESCRITA_PUNT`, `MOD_COMUNI_ESCRITA_DESEM`, `MOD_COMUNI_ESCRITA_PNAL`: Performance in written communication tests.
  - `PUNT_GLOBAL`: Global test score.
  - `PERCENTIL_NBC`: National percentile.
  - `PERCENTIL_GLOBAL`: Global percentile.

### Prediction Challenges

1. **Data Diversity:** The database includes a wide variety of features that may be correlated with obtaining scholarships, requiring careful analysis to identify the most relevant variables.
2. **Missing Values:** It is common for educational data to have missing values that need to be handled appropriately to avoid biasing the model results.
3. **Categorical Variables:** Many features are categorical and need to be transformed (e.g., one-hot encoding) to be used in a machine learning model.
4. **Class Imbalance:** The number of students receiving scholarships may be significantly lower than those not receiving scholarships, requiring special techniques to handle class imbalance in the predictive model.

## Project Strategy

### Step 1: Business and Data Understanding
- Identify the project's goal and the importance of predicting scholarship attainment.
- Describe the available features in the data and their relevance to the analysis.

### Step 2: Data Preparation
- Select and clean the data, handling missing values and transforming categorical variables into dummy variables.
- Normalize numerical features for comparable scales.

### Step 3: Model Building
- Split the data into training and test sets.
- Train a logistic regression model using the selected features.
- Evaluate the model using appropriate metrics (accuracy, recall, F1-score).

### Step 4: Results Interpretation and Communication
- Interpret the model coefficients to identify the most relevant features for predicting scholarships.
- Communicate the findings clearly to stakeholders (educational institutions, policymakers, etc.).

## Links to Notebooks

- [Logistic Regression](https://colab.research.google.com/drive/1J_d4xZbEr8LBC2ZOmmzVBNP7IZysaYcu?usp=sharing&pli=1&authuser=1)
- [Multiple Regression](https://colab.research.google.com/drive/1qEDmz7-W19vKDLBb6iycWh7WKKhvUZ0E#scrollTo=ghEwK2SxnUtR)
