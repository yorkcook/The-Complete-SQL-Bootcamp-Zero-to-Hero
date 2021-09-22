Situation 1: Create Student table with following columns

1. student_id PK
2. first_name
3. last_name
4. homeroom_number
5. phone number unique not null
6. email unique not null
7. graduation_year

Solution:

CREATE TABLE students (
student_id SERIAL PRIMARY KEY,
first_name VARCHAR(25) NOT NULL,
last_name VARCHAR(25) NOT NULL,
homeroom_number INTEGER,
phone VARCHAR(15) UNIQUE NOT NULL,
email VARCHAR(50) UNIQUE,
graduation_year INTEGER
)

Situation 2: Create Teachers table with following columns

1. teacher_id PK
2. first_name
3. last_name
4. homeroom_number
5. department
6. email unique not null
7. phone number unique not null

Solution:

CREATE TABLE teachers (
teacher_id SERIAL PRIMARY KEY,
first_name VARCHAR(25) NOT NULL,
last_name VARCHAR(25) NOT NULL,
homeroom_number INTEGER,
department VARCHAR(25),
email VARCHAR(50) UNIQUE NOT NULL,
phone VARCHAR(15) UNIQUE
)

Situation 3:

Create entry for a student named Mark Watney, homeroom 5, phone number 777-555-1234, and graduation year of 2035.

Solution:

INSERT INTO students (first_name, last_name, homeroom_number, phone, graduation_year)
VALUES ('Mark', 'Watney', 5, '7775551234', 2035)

Situation 4:

Create entry for a teacher named Jonas Salk, homeroom 5, phone number 777-555-4321, Biology department, and email jsalk@school.org.

Solution:

INSERT INTO teachers (first_name, last_name, homeroom_number, phone, department, email)
VALUES ('Jonas', 'Salk', 5, '7775554321', 'Biology', 'jsalk@school.org')
