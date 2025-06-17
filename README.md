# 📊 Productivity Survey 2017 - Power BI Report

This repository contains a Power BI report that analyzes responses from a 2017 productivity survey. The dashboard explores productivity levels, major challenges, helpful habits, and the correlation between productivity and happiness across different age groups.

---

## 🔗 Power BI Report Link

👉 [Click here to view the Power BI Report](https://app.powerbi.com/reportEmbed?reportId=d1eb515b-009c-4cf3-918d-bd0192237e39&autoAuth=true&ctid=e1d99821-ef38-4f48-836f-7a7ca113dab7)

---

## 📁 Dataset Summary

- **Source:** Simulated survey data (2017)
- **Total Respondents:** 1223
- **Key Columns:**
  - `Age`
  - `How productive do you currently feel overall?`
  - `What is the biggest challenge you face to being productive?`
  - `What is helpful in being productive?`
  - `How important is productivity to happiness?`

---

## 📊 Dashboard Features

### 1. Productivity by Age Group
- Filter slicer for age brackets: `<18`, `18–21`, `22–25`, ..., `55+`
- Dynamic visuals update based on selected group.

### 2. How productive do you currently feel overall?
- Horizontal bar chart visualizes self-assessed productivity.
- Categories: Very Productive, Moderately Productive, Unproductive, etc.

### 3. What is the biggest challenge you face to being productive?
- Pie chart showing key challenges:
  - Distractions (e.g., social media)
  - Constant interruptions
  - Time management
  - Lack of right technology
  - Other

### 4. What is helpful in being productive?
- Donut chart showcasing productivity boosters:
  - To-do lists
  - Naps
  - Exercise
  - Meditation
  - Caffeine
  - Others

### 5. How important is productivity to happiness?
- Donut chart showing respondent opinions about the connection between productivity and personal happiness.

### 6. Summary Tiles
- KPIs displaying top challenge counts and common reasons provided by respondents.

---
## DAX MEASURED USED
Here are all the measures used in this report (POWER BI )
-	 %Challange Interuptions = [Challange Interruption]/count(ProductivitySurvey2017[RespondentID])


-	Challange Distractions = CALCULATE(count(ProductivitySurvey2017[What is the biggest challenge you face to being productive?]),filter(ProductivitySurvey2017,ProductivitySurvey2017[What is the biggest challenge you face to being productive?]= "Distractions (e.g. Social Media)"))


-	Challange Interruption = CALCULATE(count(ProductivitySurvey2017[What is the biggest challenge you face to being productive?]),FILTER(ProductivitySurvey2017,ProductivitySurvey2017[What is the biggest challenge you face to being productive?] ="Constantly being interrupted by colleagues"))



-	Challange Others = CALCULATE(COUNT(ProductivitySurvey2017[What is the biggest challenge you face to being productive?]),FILTER(ProductivitySurvey2017,ProductivitySurvey2017[What is the biggest challenge you face to being productive?]="Other (please specify)"))


-	Challange Right Technology = CALCULATE(COUNT(ProductivitySurvey2017[What is the biggest challenge you face to being productive?]),FILTER(ProductivitySurvey2017,ProductivitySurvey2017[What is the biggest challenge you face to being productive?]="Not having the right technology "))

-	Challange Time Management = CALCULATE(count(ProductivitySurvey2017[What is the biggest challenge you face to being productive?]),filter(ProductivitySurvey2017,ProductivitySurvey2017[What is the biggest challenge you face to being productive?]="Time Management"))


-	Total Respondents = COUNT(ProductivitySurvey2017[RespondentID])



## 🛠 Tools and Technologies

- **Power BI Desktop**
- **DAX** for calculated measures
- Custom visualizations and data filtering

---

## 💡 Key Insights

- Most respondents feel **moderately productive**.
- **Distractions and time mismanagement** are the leading challenges.
- Simple habits like **creating to-do lists**, **short naps**, and **breaks** are helpful.
- **Majority** of participants believe productivity is directly linked to their happiness.

---

## 📌 Filters and Interactions

- Slicer: Age group
- Visual cross-filtering
- Interactive charts for drill-down analysis

---

## 👨‍💼 Author

**Created by:** Anuj Agarwal  

```bash
📁 Productivity-Survey-PowerBI
│
├── PRODUCTIVITY SURVEY.pbix      # Power BI report file
├── Productivity2017.xlsx         # Raw survey data
├── MostHelpful.xlsx              # Additional processed survey data
├── Dax.txt                       # DAX expressions used in report visuals
├── README.md                     # This file
└── assets/                       # (Optional) Screenshots of the dashboard
