# crm-data-cleaner-sql
Data Cleaning &amp; Analytics using Excel and MySQL
# 📊 CRM Data Cleaner & Analytics Project

## 🔍 Overview
This project focuses on cleaning, validating, and analyzing institutional data using Excel and MySQL.

---

## 🧹 Data Cleaning (Excel)
- Removed duplicates and handled missing values
- Standardized categorical data
- Created derived columns:
  - Total Score
  - Average Score
  - Pass/Fail classification

---

## 🗄️ Database (MySQL)
- Imported cleaned dataset into MySQL
- Designed structured table for analysis

---

## 📊 SQL Analysis
- Total student count
- Average performance
- Pass vs Fail distribution
- Gender-wise performance
- Impact of preparation course


- ## The following SQL queries were used to derive business insights from the dataset

### Total Students
SELECT COUNT(*) FROM students_final;

### Average Score
SELECT AVG(avg_score) FROM students_final;

### Pass vs Fail
SELECT pass_fail, COUNT(*) 
FROM students_final
GROUP BY pass_fail;

### Top Performers
SELECT total_score
FROM students_final
ORDER BY total_score DESC
LIMIT 10;

### Performance by Gender
SELECT gender, AVG(avg_score)
FROM students_final
GROUP BY gender;

### Impact of Preparation Course
SELECT prep_course, AVG(avg_score)
FROM students_final
GROUP BY prep_course;

---

## 📈 Key Insights
- Students who completed the preparation course scored higher on average
- High overall pass rate indicates strong academic performance
- Performance varies across demographic segments
- Gender-based trends observed in average scores

---

## 🛠️ Tools Used
- Excel
- MySQL
