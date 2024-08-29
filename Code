create database gradebook;
use gradebook;

-- Creating Students Table
CREATE TABLE Students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    date_of_birth DATE,
    email VARCHAR(100),
    major VARCHAR(100)
);

-- Creating Instructors Table
CREATE TABLE Instructors (
    instructor_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department VARCHAR(100),
    email VARCHAR(100)
);

-- Creating Courses Table
CREATE TABLE Courses(
    course_id INT AUTO_INCREMENT PRIMARY KEY,
    course_name VARCHAR(100),
    credits INT,
    department VARCHAR(100)
);



-- Creating Enrollments Table
CREATE TABLE Enrollments (
    enrollment_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    course_id INT,
    instructor_id INT,
    grade DECIMAL(4,2),
    FOREIGN KEY (student_id) REFERENCES Students(student_id),
    FOREIGN KEY (course_id) REFERENCES Courses(course_id),
    FOREIGN KEY (instructor_id) REFERENCES Instructors(instructor_id)
);

-- Creating Departments Table
CREATE TABLE Departments (
    department_id INT AUTO_INCREMENT PRIMARY KEY,
    department_name VARCHAR(100)
);
insert into departments(department_name) values("Mathematics");
insert into departments(department_name) values("Computer_Science");
insert into departments(department_name) values("Physics");
insert into departments(department_name) values("History");
insert into departments(department_name) values("Chemistry");
insert into departments(department_name) values("Biology");
insert into departments(department_name) values("Engineering");
insert into departments(department_name) values("Psychology");
insert into departments(department_name) values("Economics");
insert into departments(department_name) values("Political_Science");


-- Problem: Identify courses with the highest and lowest student enrollments
SELECT course_name, COUNT(enrollment_id) AS enrollment_count
FROM courses
JOIN enrollments ON courses.course_id = enrollments.course_id
GROUP BY course_name
ORDER BY enrollment_count DESC;
-- (Change DESC to ASC for the courses with the lowest enrollments)

-- Problem: Calculate the average grade for each course to assess overall course performance
SELECT course_name, AVG(grade) AS average_grade
FROM courses
JOIN enrollments ON courses.course_id = enrollments.course_id
GROUP BY course_name
ORDER BY average_grade DESC;

-- Problem: Determine the number of courses assigned to each instructor to evaluate workload distribution
SELECT instructors.first_name, instructors.last_name, COUNT(courses.course_id) AS course_count
FROM instructors
JOIN courses ON instructors.DEPARTMENT = courses.DEPARTMENT
GROUP BY instructors.instructor_id, instructors.first_name, instructors.last_name
ORDER BY course_count DESC;

-- Problem: Identify instructors with the highest number of student enrollments in their courses
SELECT instructors.first_name, instructors.last_name, COUNT(enrollments.enrollment_id) AS total_enrollment
FROM instructors
JOIN courses ON instructors.DEPARTMENT = courses.DEPARTMENT
JOIN enrollments ON courses.course_id = enrollments.course_id
GROUP BY instructors.instructor_id, instructors.first_name, instructors.last_name
ORDER BY total_enrollment DESC;

-- Problem: Find out how many students are enrolled in each academic major
SELECT major, COUNT(student_id) AS student_count
FROM students
GROUP BY major
ORDER BY student_count DESC;

-- Problem: Determine which departments offer the most and the least number of courses
SELECT department_name, COUNT(course_id) AS course_count
FROM departments
JOIN courses ON departments.department_id = courses.department
GROUP BY department
ORDER BY course_count DESC;
-- (Change DESC to ASC for departments offering the least number of courses)

-- Problem: Calculate the average grade of students grouped by their major
SELECT major, AVG(grade) AS average_grade
FROM students
JOIN enrollments ON students.student_id = enrollments.student_id
GROUP BY major
ORDER BY average_grade DESC;

-- Problem: Identify the number of courses offered by each department
SELECT department_name, COUNT(course_id) AS course_count
FROM departments
JOIN courses ON departments.department_id = courses.department
GROUP BY department_name
ORDER BY course_count DESC;
-- Problem: Analyze the distribution of students across different departments
SELECT departments.department_name, COUNT(students.student_id) AS student_count
FROM students
JOIN departments ON students.major = departments.department_name
GROUP BY departments.department_name
ORDER BY student_count DESC;


