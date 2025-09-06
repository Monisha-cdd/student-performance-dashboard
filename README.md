🎓 Student Performance Dashboard – Power BI
📌 Overview

This Power BI project analyzes student performance data across multiple subjects, departments, and demographic factors.
It provides insights into overall performance, subject averages, pass/fail distribution, and performance gaps.

📊 Key Insights and DAX Measures
1. Total Students

DAX Measure

Total Students = COUNTROWS(Sheet1)


Description: Counts the total number of students in the dataset.

2. Average Subject Scores

DAX Measures

Average Python Score   = AVERAGE(Sheet1[Python])
Average Math Score     = AVERAGE(Sheet1[Maths])
Average English Score  = AVERAGE(Sheet1[English])
Average EG Score       = AVERAGE(Sheet1[EngineeringGraphics])


Description: Calculates the average performance for each subject individually.

3. Overall Performance

DAX Measure:

Overall Performance = 
AVERAGE([Average Math Score]  + [Average EG Score]  + [Average English Score] + [Average Python Score]


Description: Evaluates the average performance of students across all four core subjects.

4. Performance Gap

DAX Measure

Performance Gap = [Average Math Score]   - [Average EG Score]   - [Average English Score]  - [Average Python Score]


Description: Highlights the gap in performance across subjects by comparing average Math scores with other subjects.

5. Pass Count

DAX Measure

PassCount = CALCULATE(COUNTROWS(Sheet1), Sheet1[Result] = "Pass")


Description: Counts the number of students who passed all subjects.

6. Fail Count

DAX Measure

FailCount = CALCULATE( COUNTROWS(Sheet1),  Sheet1[Result] = "Fail")


Description: Counts the number of students who failed one or more subjects.

📈 Visualization Suggestions

Total Students, Pass, Fail → KPI Cards or Gauge Charts.

Average Subject Scores → Clustered Column Chart.

Performance Gap → Waterfall Chart.

Pass vs Fail Distribution → Pie or Stacked Column Chart.

Department-wise Pass/Fail → Line and Stacked Column Chart.

🚀 Usage

Import the student dataset into Power BI.

Create the DAX measures listed above.

Add the suggested visualizations to build an interactive dashboard.

Share insights with faculty and students for performance improvements.
