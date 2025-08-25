# Titanic Data Cleaning Project

This repository contains a notebook for cleaning and preparing the Titanic dataset for analysis.

## Dataset

The original dataset used is: [Titanic Dirty Dataset](https://drive.google.com/file/d/1-7mcBguuzAV7JWVu2XCpgAO-fO6X2cl0/view?usp=sharing).

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

## Tools Used

- Python 3  
- Pandas  
- NumPy  
- Missingno for visualizing missing values  

## Outcome

The cleaned dataset is ready for analysis with no missing values in numeric/object columns (except placeholders) and consistent categorical values.

## Author

- Bashar Bayatna
