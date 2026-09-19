# Python & Data Wrangling Assignment

This directory contains the Python implementation for data loading, data cleaning, feature engineering, and data visualization using Pandas, Matplotlib, and Seaborn.

## 📁 Repository Structure
- `Data_Cleaning.ipynb`: Jupyter Notebook containing step-by-step Python code with comments.
- `Cleaned_Fitness_Data.csv`: Processed output dataset after handling missing values and data formatting.

## 🛠️ Key Tasks Completed
1. **Data Cleaning & Preprocessing:**
   - Standardized column headers and stripped unnecessary whitespace.
   - Fixed missing and improperly formatted values in the `Date` column using forward fill (`ffill`).
   - Imputed missing values in the `Calories` column using median values.

2. **Outlier Treatment & Deduplication:**
   - Handled duration outliers (`> 120` mins) using median replacement.
   - Removed duplicate records to ensure data integrity.

3. **Feature Engineering:**
   - Created `Total_Workout_Hours` (`Duration / 60`).
   - Created `Calories_Per_Min` (`Calories / Duration`).

4. **Data Visualization:**
   - Built a **Line Plot** using Matplotlib to track calorie burn trends.
   - Built a **Scatter Plot** using Seaborn to analyze the relationship between Pulse Rate and Calories Burned.

## 🚀 Environment & Libraries Used
- **Language:** Python 3.x
- **Environment:** VS Code (Jupyter Notebooks)
- **Libraries:** Pandas, Matplotlib, Seaborn
-
