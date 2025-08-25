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

8. **Saved Cleaned Dataset**
   - Exported the cleaned DataFrame to a CSV for future analysis.

9. **Univariate Plots and Multivariate Plots**  

     

## Visualization and Key Insights

1. **Count of Survived vs Died Passengers**  
   <img width="571" height="455" alt="Passengers State" src="https://github.com/user-attachments/assets/ab7b4908-70fb-4323-bc5b-6b803e4870b9" />


  Died: 549 passengers
  Survived: 342 passengers
  More passengers died than survived on the Titanic.

2. **Histogram of Age Distribution**

    <img width="571" height="455" alt="Age Distribution" src="https://github.com/user-attachments/assets/cdbfd549-b02b-4dbb-b384-546038643bb2" />

   Majority of passengers were between 20–40 years old.
   177 passengers had missing Age values (filled with -1).
3. **Boxplot of Fare**
    <img width="520" height="455" alt="BoxPlot of the Fare" src="https://github.com/user-attachments/assets/172ff1bf-2ccd-495b-8594-48b0046428d3" />

   Fare ranged from $0 to $512.33.
   Median fare is around $14.45.
   Presence of outliers shows some passengers paid very high fares.

4. **Passengers by Sex**

   Male: 574 passengers
   Female: 317 passengers

5. **Embarked Locations**

  - S: 644 passengers
  - C: 168 passengers
  - Q: 77 passengers
  - Missing: 2 passengers


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

   
   
