# DAX Measures (adjust field names as needed)
```
Total Exams = COUNTROWS(FactStudentPerformance)
Average Score = AVERAGE(FactStudentPerformance[Score])
Pass Count = COUNTROWS(FILTER(FactStudentPerformance, FactStudentPerformance[Score] >= 50))
Pass Rate % = DIVIDE([Pass Count], [Total Exams])

Score YoY = CALCULATE([Average Score], DATEADD(DimDate[Date], -1, YEAR))
Score YoY % = DIVIDE([Average Score] - [Score YoY], [Score YoY])

Average Score by Subject = AVERAGEX(VALUES(DimSubject[Subject]), [Average Score])
```
