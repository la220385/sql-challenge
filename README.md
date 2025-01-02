# Pewlett Hackard Employee Database

## Overview
This module Challenge involves creating a relational database for Pewlett Hackard to analyze employee data from the 1980s and 1990s. This includes designing a database schema, importing data from CSV files, and performing queries to answer specific business questions.

## Deliverables
1. **Entity Relationship Diagram (ERD):** Visual representation of the database schema, showing relationships between tables.
2. **Schema File (`Table_schema.sql`):** Contains SQL statements to create the tables with appropriate primary and foreign keys.
3. **Queries File (`queries.sql`):** Contains SQL queries to extract specific information from the database.
4. **SQLite Database (`PewlettHackardDB.sqlite`):** Fully populated SQLite database containing all employee data.

## Database Structure
The database contains the following tables:

1. **departments**:
   - `dept_no` (Primary Key)
   - `dept_name`

2. **dept_emp**:
   - `emp_no` (Primary Key, Foreign Key to `employees.emp_no`)
   - `dept_no` (Primary Key, Foreign Key to `departments.dept_no`)

3. **dept_manager**:
   - `dept_no` (Primary Key, Foreign Key to `departments.dept_no`)
   - `emp_no` (Primary Key, Foreign Key to `employees.emp_no`)

4. **employees**:
   - `emp_no` (Primary Key)
   - `emp_title_id` (Foreign Key to `titles.title_id`)
   - `birth_date`
   - `first_name`
   - `last_name`
   - `sex`
   - `hire_date`

5. **salaries**:
   - `emp_no` (Primary Key, Foreign Key to `employees.emp_no`)
   - `salary`

6. **titles**:
   - `title_id` (Primary Key)
   - `title`

## Queries Included
The following queries are included in the `queries.sql` file:

1. List employee details (employee number, last name, first name, sex, and salary).
2. List employees hired in 1986 (first name, last name, and hire date).
3. List department managers with department details.
4. List department details for each employee.
5. List employees whose first name is \"Hercules\" and last name starts with \"B.\"
6. List employees in the \"Sales\" department.
7. List employees in \"Sales\" and \"Development\" departments.
8. Frequency count of employees sharing the same last name.

## Steps to Run the Project
1. **Database Setup:**
   - Use the `Table_schema.sql` file to create the database schema.
   - Import the data into the database using SQLite tools or scripts.
2. **Run Queries:**
   - Use the `queries.sql` file to run predefined queries and extract insights.

## Resources Used
1. **SQLite Documentation**: [https://sqlite.org/docs.html](https://sqlite.org/docs.html)
2. **DB Browser for SQLite**: [https://sqlitebrowser.org/](https://sqlitebrowser.org/)
3. **QuickDBD**: [https://www.quickdatabasediagrams.com/](https://www.quickdatabasediagrams.com/)
4. **W3Schools SQL Tutorial**: [https://www.w3schools.com/sql/](https://www.w3schools.com/sql/)
5. **Python (Optional for Automation)**:
   - pandas Library: [https://pandas.pydata.org/](https://pandas.pydata.org/)
   - sqlite3 Module: [https://docs.python.org/3/library/sqlite3.html](https://docs.python.org/3/library/sqlite3.html)
7. **Stack Overflow**: [https://stackoverflow.com/](https://stackoverflow.com/)
8. **Lucidchart ERD Guide**: [https://www.lucidchart.com/pages/er-diagram-symbols-and-meaning](https://www.lucidchart.com/pages/er-diagram-symbols-and-meaning)
9. **SQLite Cheatsheet**: [https://cheatography.com/davechild/cheat-sheets/sqlite/](https://cheatography.com/davechild/cheat-sheets/sqlite/)

## ERD Image
The ERD image (`Entity Relationship Diagram.png`) visually explains the relationships between the tables.

## Files in the Repository
- `Entity Relationship Diagram.png`: Visual representation of the database schema.
- `Table_schema.sql`: SQL script for creating database tables.
- `queries.sql`: SQL script containing predefined queries.
- `PewlettHackardDB.sqlite`: SQLite database with imported data.