<<<<<<< HEAD
## Goal
The goal for this analysis was to investigate patient cohorts based on their BMI rangesand get summary statistics. 
## Steps Taken
=======
## Analysis Approach 
Data Preparation and Cleaning:
1. Converted CSV to Parquet: I converted the csv to parquet so that it would be more efficient and processes faster because we are dealing with a big dataset.
2. Filtering BMI: I only kept the BMI values between 10 and 60. 
3. BMI Categorization: The BMI values were clasified into meaningful categories (underweight, normal, overweight, obese) to make the analysis more interpretable. 

The analysis calculates the average glucose, patient count, and average age for each BMI catgeory which will help us identify trends. 

## Patterns and Insights 
1. Medication Specific Adjustments:
The dosage logic varies depending on the medication. For example, epinephrine was given based off patient weight like John Smith who was given the standard dosage of 0.80 mg. Amiodarone requires a loading dose which doubles it. So Sarah got 600 mg instead of 300 mg. 
2. Clinical Warnings:
Each medication has its own clinical warnings. Epinephrine warns about arrhythmias and amiodarone warns for hypotension. These warnings ensures patients and doctors for the potential risks. 
3. Glimpse into Patient Profiles: 
We can see some patterns emerging such as more intense medications are usually associated with additional precaustions and higher dosage. 
4. Total medication needed:
The script also provides the total medication required across all patients. This is useful for inventory management.

## Polars Features for Efficiency
The reason why Polars was used is because it so much faster and has more memory efficiency. This is really important when we are dealing with large datasets. When you convert it from csv to parquet it will improve read speeds and in general speed up data processing. 

Another method that was used was .pipe(). This was used to chain transformations in a clean and readable way. It prevents clutter, keeps the logic modular, and makes sures that each transformation is applied in an optimized order. 

The pl.col("BMI") function makes sure to catgeorize continious BMI values into bins that we made. This insures that there wouldn't be any slow loops or manual conditionals. 
These features makes sure that the analysis is suitable for large patient datasets and in faster time. 
>>>>>>> 60a7d421af162a4f0c3e8add41759177a3335bdf
