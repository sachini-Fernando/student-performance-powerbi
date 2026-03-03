# Student Performance Prediction & At-Risk Analysis Dashboard (Power BI)
## 📊 Project Overview
This project presents a Power BI dashboard designed to analyze and predict student final exam performance. The dashboard identifies at-risk students, analyzes key influencing factors, and monitors grade progression.

The system helps educators understand student behavior and take early actions to improve academic performance.

## 🎯 Project Objectives
- Predict final exam performance (G3)
- Identify at-risk students
- Analyze factors affecting grades
- Monitor student progress
- Visualize academic trends
- Support early intervention decisions

## 🛠 Tools & Technologies
 - Power BI
 - DAX (Data Analysis Expressions)
 - CSV Dataset
 - Data Visualization

## 📁 Dataset Description
  The dataset contains student academic and behavioral data.

### Main Variables
| Column | Description |
| G1	       |      First period grade |
| G2	       |      Second period grade |
| G3	       |       Final grade |
| studytime	  |      Weekly study time |
| absences	  |      Number of absences |
| failures	  |      Past class failures |
| Medu	      |      Mother education |
| Fedu	      |     Father education | 
| goout	      |     Going out with friends |
| Walc	      |     Weekend alcohol consumption |
| sex	        |     Gender | 
| school	    |     School name |

Dataset Size:

649 students (sampled dataset)

## 📈 Dashboard Pages
&#9734; Affecting Factors for Exam Scores
- This page analyzes factors that influence student performance.

  ### Visualizations:
    - Key Influencers Visual
    - Study Time vs Grades
    - Absences vs Grades
    - Failures vs Grades
    - Parent Education vs Grades

  ### insights:
  - Higher study time improves grades
  - More absences reduce performance
  - Past failures lower final scores

&#9734; Predict Final Exam Performance
- This page predicts final exam results.

  ### Visualizations:
    - Grade Progression Line Chart
    - Scatter Plot (Absences vs Final Grade)
    - Prediction Table
    - KPI Cards

  ### KPIs:
    - Average Final Grade
    - Average Study Time
    - Average Absences

  ### DAX Measures
    - Avg G3 = AVERAGE(StudentData[G3])
    - Avg Study = AVERAGE(StudentData[studytime])
    - Avg Absences = AVERAGE(StudentData[absences])

&#9734; Identify At-Risk Students
- This dashboard identifies students who may fail the final exam.
- A student is considered At-Risk if Final Grade (G3) < 10

  ### KPI Cards
    - Number of At-Risk Students
    - At-Risk Percentage
    - Average Final Grade
    - Average Absences

  ### DAX Measures Used
    - Average Final Grade
        - Avg G3 = AVERAGE(StudentData[G3])
    - Average Study Time
        - Avg Study = AVERAGE(StudentData[studytime])
    - Average Absences
        - Avg Absences = AVERAGE(StudentData[absences])
    - At-Risk Students Count
       -  AtRisk Count =
        CALCULATE(
        COUNT(StudentData[G3]),
        StudentData[G3] < 10
        )
    - At-Risk Percentage
       -  AtRisk % =
        DIVIDE(
        [AtRisk Count],
        COUNT(StudentData[G3])
        ) * 100
    - At-Risk Category Column
       -  AtRisk =
        IF(StudentData[G3] < 10,
        "At Risk",
        "Not At Risk")
        
# 📉 Grade Progression Visualization
  #### Visual Type:  - Line Chart
  #### Axis: -  Grade Period (G1, G2, G3)
  #### Values: - Average Grade

This chart shows how student grades change across the academic year.

# 📊 Key Influencing Factors
  #### Visual Type: Key Influencers Visual
  #### Target: G3
  #### Factors:
        - studytime
        - absences
        - failures
        - Medu
        - Fedu
        - Walc
        - goout

This visual identifies the most important factors affecting final exam performance.

# ⚠ At-Risk Student Monitoring Dashboard
This dashboard helps teachers quickly identify students who need support.

  ### Visualizations
      - At-Risk Distribution Chart
      - Study Time vs At-Risk Students
      - Failures vs At-Risk Students
      - Absences vs At-Risk Students
      - At-Risk by Gender
      - Student Table

   ### KPIs
      - At-Risk Students
      - At-Risk Percentage
      - Average Final Grade
      - Average Absences

# 📊 Project Features

✔ Student Performance Prediction
✔ At-Risk Student Detection
✔ Interactive Dashboards
✔ KPI Monitoring
✔ Influencing Factors Analysis
✔ Grade Progression Analysis

# 🎯 Key Insights
  - Students with higher study time achieve better grades
  - Students with many absences perform worse
  - Previous failures strongly affect final grades
  - Social activities influence performance
  - Early monitoring reduces failure risk

# 👨‍💻 Author

Sachini Fernando

Student Performance Analysis Project | Power BI Dashboard Project
    
