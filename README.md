## Student-Gradebook
#Problem Statement
Objective: The goal is to develop a comprehensive and realistic dataset for a university management system. This dataset will be used for various data management and analysis tasks, including student enrollment, course management, instructor assignments, and departmental organization. The data should be generated in a format suitable for importing into a relational database for further analysis and application.
Components:

Students Data:

Description: Generate a dataset of 1500 students, each with a unique identifier, name, date of birth, email address, and major.
Fields:
student_id: Unique identifier for each student (integer).
first_name: First name of the student (string).
last_name: Last name of the student (string).
date_of_birth: Birth date of the student (date).
email: Email address of the student (string).
major: Academic major of the student (string).
Instructors Data:

Description: Create a dataset of instructors, including their unique identifier, name, department, and email address.
Fields:
instructor_id: Unique identifier for each instructor (integer).
first_name: First name of the instructor (string).
last_name: Last name of the instructor (string).
department: Department to which the instructor belongs (string).
email: Email address of the instructor (string).
Courses Data:

Description: Generate a dataset of courses offered by the university, including unique identifiers, names, credit hours, and associated departments.
Fields:
course_id: Unique identifier for each course (integer).
course_name: Name of the course (string).
credits: Number of credits for the course (integer).
department: Department offering the course (string).
Departments Data:

Description: Create a dataset of departments within the university, including unique identifiers and department names.
Fields:
department_id: Unique identifier for each department (integer).
department_name: Name of the department (string).
Enrollments Data:

Description: Generate a dataset of student enrollments in courses, including unique enrollment identifiers, student IDs, course IDs, instructor IDs, and grades.
Fields:
enrollment_id: Unique identifier for each enrollment (integer).
student_id: Identifier for the student (integer).
course_id: Identifier for the course (integer).
instructor_id: Identifier for the instructor (integer).
grade: Grade received by the student (decimal).
Requirements:

The data should be generated and saved in Excel files for each component.
The data should be realistic and consistent, with unique identifiers and appropriate field values.
Ensure that the generated data maintains referential integrity (e.g., student IDs, course IDs, and instructor IDs should match existing records).
