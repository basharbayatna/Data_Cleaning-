# Titanic Data Cleaning Project

This repository contains a notebook for cleaning and preparing the Titanic dataset for analysis. It also includes basic dataset exploration and critical visualizations to understand passenger demographics, survival, and fare patterns.


## Dataset

The original dataset used is: [Titanic Dirty Dataset](https://drive.google.com/file/d/1-7mcBguuzAV7JWVu2XCpgAO-fO6X2cl0/view?usp=sharing).

**Basic Dataset Information:**

- **Rows:** 891  
- **Columns:** 12  
- **Features include:** `PassengerId`, `Survived`, `Pclass`, `Sex`, `Age`, `Siblings or Spouses`, `Parents or Children`, `Fare`, `Embarked`, etc.

**Sample Data:**

| PassengerId | Survived | Pclass | Sex    | Age  | Siblings or Spouses | Parents or Children | Fare  | Embarked |
|------------:|---------:|-------:|--------|-----:|------------------:|------------------:|------:|---------|
| 1           | 0        | 3      | male   | 22.0 | 1                 | 0                 | 7.25  | S        |
| 2           | 1        | 1      | female | 38.0 | 1                 | 0                 | 71.28 | C        |
| 3           | 1        | 3      | female | 26.0 | 0                 | 0                 | 7.93  | S        |
| 4           | 1        | 1      | female | 35.0 | 1                 | 0                 | 53.10 | S        |
| 5           | 0        | 3      | male   | 35.0 | 0                 | 0                 | 8.05  | S        |


## What I Did

1. **Loaded the Data**  
   - Read the CSV into a Pandas DataFrame and displayed the first and last rows.  
   - Checked data types, column info, and initial statistics.

2. **Checked and Fixed Data Types**  
   - Converted `Fare` from string to float by removing `$` signs.  
   - Fixed `SibSp` to numeric type and corrected mis-typed entries (`one → 1`).  

3. **Dropped and Renamed Columns**  
   - Dropped unnecessary column `Unnamed: 0`.  
   - Renamed `SibSp` → `Sibilings` and `Parch` → `Parents` for clarity.

4. **Handled Duplicates**  
   - Identified and removed 30 duplicate rows.

5. **Set Index and Dropped `Name` Column**  
   - Set `PassengerId` as the index for easier referencing.  
   - Dropped `Name` as it was not required for analysis.

6. **Handled Missing Values**  
   - Filled missing `Cabin` and `Embarked` values with `"MISSING"`.  
   - Filled missing `Age` values with `-1` as a placeholder.

7. **Ensured Consistency**  
   - Corrected inconsistent values: `Sex` (F → female) and `Embarked` (Queenstown → Q).  


8. **Univariate Plots and Multivariate Plots**  

     

## Visualization and Key Insights

1. **Count of Survived vs Died Passengers by Sex**  
   <img width="571" height="455" alt="Passengers Status By Sex" src="https://github.com/user-attachments/assets/f8cf1d74-4ca6-46e4-a090-d71338e0ae71" />


  - Number of passengers died: 549 passengers
  - Number of passengers Survived: 342 passengers where 250 of them are Females.

2. **Histogram of Age Distribution**

    <img width="571" height="455" alt="Age Distribution" src="https://github.com/user-attachments/assets/cdbfd549-b02b-4dbb-b384-546038643bb2" />

 - Majority of passengers were between 20–40 years old.
   177 passengers had missing Age values (filled with -1).
   
4. **Heatmap**
    <img width="838" height="528" alt="Correlation heatmap" src="https://github.com/user-attachments/assets/899b6a6b-5c04-4b53-ab72-c56bfca4d755" />

    - The Fare has The Highest Positive Correlation to the Survived Column

   

## Tools Used

- Python 3
- Pandas
- NumPy
- Seaborn & Matplotlib
- Missingno for visualizing missing values

## Outcome

- The cleaned dataset is ready for analysis.  
- All numeric and object columns have no missing values except placeholder `-1` for `Age`.  
- Categorical values are consistent.  
- Univariate visualizations provide clear insights into distributions and outliers.  
- Critical visualizations helped understand passenger survival, demographics, and fare trends.

## Author

  Bashar Bayatna
- Basharbayatna11@gmail.com

   
   
