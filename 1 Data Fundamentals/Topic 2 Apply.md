
1. What is the usability score of this dataset and is it “good” or “bad”?
   - Bad, missing provenance, no update frequency, low tag rating for clean data. High on completeness and compatability, low on credibility
2. How is this usability score calculated?
3. What are the two credibility issues with this dataset and why are they important? Missing provenance, no update frequency
4. How many columns does this dataset have? 35
5. What is the licence for this dataset and how would you summarise the usage rights in your own words? Open License, free to use the data. Does not cover the database itself, just the contents

![image](https://github.com/user-attachments/assets/69fb1d9d-3135-4b9e-97db-1a62398e511d)

Md5 - checksum to verify data integrity
Boolean - in Attrition column One of 2 values, Yes/No, 0/1, True/False
Integer - Whole number. Used in Age column

6. Why does using compression aid sustainability and net-zero goals? Smaller file size requiring less processing and network power
7. Compare the contents of the column 'Over18' and 'OverTime', what data quality issue can you identify?
- Look to be potential Boolean format but Yes used in Overtime and Y used in Over 18

8. What are some possible issues with the data quality of 'MonthlyIncome' and 'Monthly Rate'? 
- Look to be integer fields, should be number fields if we were to use this field in calculations.

9. How would you validate the 'EmployeeNumber' column and what needs paying special attention to? 
- Employee ID maybe sequential, would need to check that every employee ID was showing in the file (eg 3 is missing)

https://github.com/MarkToddEE/Learning-Journal/blob/main/1%20Data%20Fundamentals/IBM%20data.xlsx

# KSB's
K1
Processes to monitor and optimise the performance of the availability, management 
and performance of data product. 
S6
Systematically clean, validate, and describe data at all stages of extract, transform, load 
(ETL).
