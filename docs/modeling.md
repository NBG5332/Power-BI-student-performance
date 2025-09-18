# Data Modeling (Star Schema)

**Target model**: 1 fact + 4 dimensions

- **FactStudentPerformance**: student × subject × exam row, column: Score
- **DimStudent**: ['gender', 'race_ethnicity', 'parental_level_of_education', 'lunch', 'test_preparation_course']
- **DimSubject**: from unpivot of ['math_score', 'reading_score', 'writing_score']
- **DimDate**: ['AcademicYear']
- **DimSchool**: ['School', 'Class', 'Section']

## Power Query steps (M)
1. Select subject score columns and **Unpivot Columns** to long format → `Subject`, `Score`.
2. Create surrogate keys for Student, Subject, Date, School.
3. Mark DimDate as **Date table** (Power BI).
4. Set one-to-many relationships to the Fact table (single direction).