Create the database
CREATE DATABASE college_2; new database named college_2.
Use the database
USE college_2; selects the college_2 database so that all tables are created inside it.
Create the Department table
The Department table stores department details. dept_id is the primary key, and dept_name must be unique and not null.
Create the Student table
Student_2 stores student information such as roll number, name, email, Aadhaar number, and department ID. roll_no is the primary key.
Use constraints for student data
NOT NULL ensures required values are entered, while UNIQUE ensures that email and Aadhaar numbers cannot be duplicated.
Create a relationship between Student and Department
dept_id in Student_2 is a foreign key referencing Department(dept_id). This connects each student to a department.
Create the Course table
The Course table stores course ID, course name, and department ID. course_id is the primary key, and dept_id connects the course to a department.
Create the Enrollment table
Enrollment stores which student takes which course, along with the semester and grade. It uses roll_no and course_id as foreign keys.
Apply semester and primary-key rules
CHECK (semester between 1 and 8) allows only semesters 1 through 8. The combined primary key (roll_no, course_id, semester) prevents the same student from enrolling in the same course twice in the same semester.
Insert sample records
The code inserts departments, students, courses, and enrollments. For example, student 101 (Nilisha) is enrolled in DBMS and Circuits during semester 3, which is allowed because the courses are different.
