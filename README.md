## Student-Gradebook
Introduction
This project involves analyzing a comprehensive grade book dataset for a university. The dataset includes detailed information about students, instructors, courses, enrollments, and departments. The aim is to explore and extract meaningful insights from the data to enhance academic performance monitoring, optimize resource allocation, and improve overall educational outcomes. By examining enrollment patterns, course performance, instructor workloads, and student distributions, this analysis seeks to provide actionable recommendations for academic management and decision-making.
Table Creation
I started by creating a database called Gradebook to store the data set. The tables 

 Data Components:
Note: This is a real world problem but I generated my own dataset using python
1.	Students Data:
o	Description: Generate a dataset of 1500 students, each with a unique identifier, name, date of birth, email address, and major.
o	Fields:
	student_id: Unique identifier for each student (integer).
	first_name: First name of the student (string).
	last_name: Last name of the student (string).
	date_of_birth: Birth date of the student (date).
	email: Email address of the student (string).
	major: Academic major of the student (string).
2.	Instructors Data:
o	Description: Create a dataset of instructors, including their unique identifier, name, department, and email address.
o	Fields:
	instructor_id: Unique identifier for each instructor (integer).
	first_name: First name of the instructor (string).
	last_name: Last name of the instructor (string).
	department: Department to which the instructor belongs (string).
	email: Email address of the instructor (string).
3.	Courses Data:
o	Description: Generate a dataset of courses offered by the university, including unique identifiers, names, credit hours, and associated departments.
o	Fields:
	course_id: Unique identifier for each course (integer).
	course_name: Name of the course (string).
	credits: Number of credits for the course (integer).
	department: Department offering the course (string).
4.	Departments Data:
o	Description: Create a dataset of departments within the university, including unique identifiers and department names.
o	Fields:
	department_id: Unique identifier for each department (integer).
	department_name: Name of the department (string).
5.	Enrollments Data:
o	Description: Generate a dataset of student enrollments in courses, including unique enrollment identifiers, student IDs, course IDs, instructor IDs, and grades.
o	Fields:
	enrollment_id: Unique identifier for each enrollment (integer).
	student_id: Identifier for the student (integer).
	course_id: Identifier for the course (integer).
	instructor_id: Identifier for the instructor (integer).
	grade: Grade received by the student (decimal).
SQL SCRIPTS AND PYTHON SCRIPT
All sql and python scripts used for data creation and processing are provided in the scripts directory this scripts can be executed in a mysql environment to replicate these steps

ANALYSIS AND INSIGHTS
I conducted an indepth analysis on the dataset to extract meaningful insights that could aid decision making and project management. This include formulating sql queries to answer key question such as
•  Which courses have the highest and lowest enrollment numbers?
•  What is the average grade for each course?
•  How many courses are assigned to each instructor?
•  Which instructors have the highest student enrollments in their courses?
•  How many students are enrolled in each major?
•  Which departments offer the most and least number of courses?
•  What is the average grade of students by major?
•  How many courses are offered by each department?
•  Which students have missing or invalid email addresses?
•  Which courses have the highest failure rates?
•  How does the distribution of students differ across departments?
