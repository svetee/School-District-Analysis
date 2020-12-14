# School_District_Analysis

## Project Overview
The school board has notified Maria and her supervisor that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to Maria for help. She has asked you to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. 

## Resources
- Data Source: schools_complete.csv, students_complete.csv

## Challenge Overview
Due to academic dishonesty at Thomas High School, the data for the math and reading scores must be removed and the following information should be recreated:

1. District and school summary
2. Top 5 and bottom 5 performing schools.
3. Average math score received by students in each grade level at each school
4. Average reading score received by students in each grade level at each school
5. School performance based on the spending per student
6. School performance based on the size of the school
7. School performance based on the type of school.

## Results 

**District summary**
            - **OLD**
            - Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
            - 79.0, 81.9, 75, 86, 65
            - **NEW**
            - Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
            - 78.9, 81.9, 74, 85, 64
            - **Result:** Slight decreased change 
        - **School summary**
            - OLD: 91% overall passing (math), second rank
            - NEW: 65% Overall Passing (math)= , eighth rank
            - **Result:** Lower rank from 2nd 
    - Recalculate high- and low-performing schools.
            - **Result:** Relative ranking for THOMAS HS changed from 2nd to 8th, with a decreased % OVERALL PASSING from 91% to 65%.
    - Recalculate the scores by grade, scores by school spending, scores by school size, and scores by school type.
        - **Replacing the ninth-grade scores**
            - **Math and Reading Scores by Grade**
                - Both scores set to "nan" and equivalent to 0
                - Average scores calculation not much affected by removal of 9th grade scores, seems due to count() function NOT including 9th grade scores = nan
                - OLD: Thomas High School       1635
                - NEW: Thomas High School       1174
            - **Scores by School Spending**
                - Thomas HS spending: "$630-644"
                - Removing 9th grade scores reduces  "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for spending bucket "$630-644":
                - OLD: 73, 84, 63
                - NEW: 67, 77, 56
            - **Scores by School Size**
                - Thomas HS is in the "Medium (1000-2000)" size bucket
                - Removing 9th grade scores reduces  "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for size bucket "Medium (1000-2000)":
                - OLD:94, 97, 91 
                - NEW: 88, 91, 85
            - **Scores by School Type**
                - Thomas HS is in the "CHARTER" bucket
                - Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for type bucket "CHARTER":
                - OLD:94, 97, 90 
                - NEW: 90	93	87

## Challenge Summary - Four Major changes
1. The percentage of students passing math and reading decreased by 1% aeach. The overall passing percentage decreased by 1%.
2. The school summary wasnt afftected, only change for TH School with a decreased math and reading passing %.
3. Thomas High School moved from 2nd place overall with a passing % of ~92% down to last place with a passing % of ~68%.
4. The Charter schools saw a decrease in the passing percentages since Thomas High School was in that school type
