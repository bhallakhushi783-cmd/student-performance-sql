Student Performance Analysis using SQL

Problem Statement

The objective of this project is to analyze student performance data and extract meaningful insights such as top-performing students and city-wise performance.

---

Dataset Description

Students Table

- id – Unique student ID
- name – Student name
- city – City of the student

Marks Table

- id – Student ID
- subject – Subject name
- marks – Marks obtained

---

SQL Concepts Used

- JOIN
- GROUP BY
- HAVING
- ORDER BY
- Aggregate Functions (AVG, MAX)

---

SQL Queries

Average Marks per Student

SELECT students.name, AVG(marks.marks) AS avg_marks
FROM students
JOIN marks ON students.id = marks.id
GROUP BY students.id, students.name;

---

Students with Average Marks > 80

SELECT students.name, AVG(marks.marks) AS avg_marks
FROM students
JOIN marks ON students.id = marks.id
GROUP BY students.id, students.name
HAVING AVG(marks.marks) > 80;

---

Top Performing Student

SELECT students.name, AVG(marks.marks) AS avg_marks
FROM students
JOIN marks ON students.id = marks.id
GROUP BY students.id, students.name
ORDER BY avg_marks DESC
LIMIT 1;

---

Average Marks by City

SELECT students.city, AVG(marks.marks) AS avg_marks
FROM students
JOIN marks ON students.id = marks.id
GROUP BY students.city;

---

[9:15 pm, 05/04/2026] ..: Best Performing City

SELECT students.city, AVG(marks.marks) AS avg_marks
FROM students
JOIN marks ON students.id = marks.id
GROUP BY students.city
ORDER BY avg_marks DESC
LIMIT 1;

---

Insights

- The top-performing student has the highest average marks
- Certain cities show better overall academic performance
- Students with average marks above 80 can be considered high performers

---

Conclusion

This project demonstrates how SQL can be used to analyze structured data and generate useful insights.

---

Sample Output

Top Performing Student:
Name: Rahul Sharma
Average Marks: 88.5

Best Performing City:
City: Delhi
Average Marks: 84.2

Students with Average Marks > 80:
Rahul Sharma
Priya Singh
Amit Verma

---
Best Performing City

SELECT students.city, AVG(marks.marks) AS avg_marks
FROM students
JOIN marks ON students.id = marks.id
GROUP BY students.city
ORDER BY avg_marks DESC
LIMIT 1;

---

Insights

- The top-performing student has the highest average marks
- Certain cities show better overall academic performance
- Students with average marks above 80 can be considered high performers

---

Conclusion

This project demonstrates how SQL can be used to analyze structured data and generate useful insights.# student-performance-sql
SQL project analyzing student performance
