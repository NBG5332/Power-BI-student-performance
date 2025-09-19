# Student Performance – Power BI Dashboard

Interactive Power BI dashboard analyzing student outcomes with a **star schema** (1 fact + 4 dimensions).

**Report**: `dashboard/student-performace.pbix`  
**Data**: `data/study_performance.csv`

## Highlights
- Modeled the dataset as a **star schema** and optimized relationships.
- Built core **DAX** for KPIs: Average Score, Pass Rate, YoY deltas.
- Added **Power Query** transformations (unpivot, data types, keys).
- Curated slicers for Subject, Gender, Ethnicity, Test Prep.

## Schema (star)
```
DimStudent   1 ─── *  FactStudentPerformance  * ─── 1  DimSubject
DimDate      1 ─── *                         * ─── 1  DimSchool
```
- Fact fields: StudentKey, SubjectKey, DateKey, SchoolKey, Score
- See `docs/modeling.md` for details.

## How to open
1. Open `dashboard/student-performace.pbix` in Power BI Desktop.
2. If prompted, point to `data/study_performance.csv`.
3. Review relationships; refresh the model.

## Repo
```
powerbi-student-performance/
├─ README.md
├─ dashboard/
│  └─ student-performace.pbix
├─ data/
│  └─ study_performance.csv
├─ docs/
   ├─ data_dictionary.md
   ├─ modeling.md
   └─ dax_measures.md

```
