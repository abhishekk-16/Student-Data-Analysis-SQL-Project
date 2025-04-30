# Student-Data-Analysis-SQL-Project

## PROJECT OVERVIEW:

This project is designed to demonstrate SQL skills and techniques typically used by data analysts to explore, clean, and analyse student data. The project involves setting up a student database, performing exploratory data analysis (EDA), and answering specific questions through SQL queries. 

## OBJECTIVES:

1. **Set up a student database**: Creating and populating a student database with the provided student data.
2. **Data cleaning**: Identifying and removing any records with missing or null values.
3. **Exploratory Data Analysis (EDA)**: Performing basic EDA to understand the dataset.
4. **Data Analysis**: using SQL to answer specific questions and derive insights from the student data.

## PROJECT STRUCTURE:

### 1. Database Setup

   - **Database creation**: Project starts by creating a database named `student_project_db` .
   - **Table creation**: A table named `student_data` is created to store the student data.

```sql
CREATE DATABASE student_project_db;

CREATE TABLE student_data
(
      student_id VARCHAR(20) PRIMARY KEY,
      first_name VARCHAR(50),
      last_name VARCHAR(50),
      email VARCHAR(50),
      gender VARCHAR(10),
      age INT,
      department VARCHAR(20),
      attendance DOUBLE,
      midterm_score DOUBLE,
      final_score DOUBLE,
      assignment_avg DOUBLE,
      quizzes_avg DOUBLE,
      participation_score DOUBLE,
      project_score DOUBLE,
      total_score DOUBLE,
      grade VARCHAR(10),
      study_hours_per_week DOUBLE,
      extracurricular_activities VARCHAR(10),
      internet_access_at_home VARCHAR(10),
      parent_education_level VARCHAR(50),
      family_income_level VARCHAR(10),
      stress_level INT,
      sleep_hours_per_night DOUBLE
);
```

### 2. Data Exploration and Cleaning

- **Record Count**: Determining the total number of record in dataset.
- **Null Value Check**: Checking for any null values in dataset and creating two tables `student_data_valid` for records without any null values and `student_data_invalid` for records having null values.

```sql
SELECT COUNT(*) FROM student_data ;

-- Finding records with any null values
SELECT * 
FROM student_data
WHERE
    student_id IS NOT NULL
    AND 
    first_name IS NOT NULL
    AND 
    last_name IS NOT NULL
    AND
    email IS NOT NULL
    AND
    gender IS NOT NULL
    AND
    age IS NOT NULL
    AND
    department IS NOT NULL
    AND
    attendance IS NOT NULL
    AND
    midterm_score IS NOT NULL
    AND
    final_score IS NOT NULL
    AND
    assignment_avg IS NOT NULL
    AND
    quizzes_avg IS NOT NULL
    AND
    participation_score IS NOT NULL
    AND
    project_score IS NOT NULL
    AND
    total_score IS NOT NULL
    AND
    grade IS NOT NULL
    AND
    study_hours_per_week IS NOT NULL
    AND
    extracurricular_activities IS NOT NULL 
    AND
    internet_access_at_home IS NOT NULL
    AND
    parent_education_level IS NOT NULL
    AND
    family_income_level IS NOT NULL
    AND
    stress_level IS NOT NULL
    AND
    sleep_hours_per_night IS NOT NULL ;

-- Creating student_data_valid table
CREATE TABLE student_data_valid as
SELECT * 
FROM student_data
WHERE
    student_id IS NOT NULL
    AND 
    first_name IS NOT NULL
    AND 
    last_name IS NOT NULL 
    AND
    email IS NOT NULL
    AND
    gender IS NOT NULL
    AND
    age IS NOT NULL
    AND
    department IS NOT NULL
    AND
    attendance IS NOT NULL
    AND
    midterm_score IS NOT NULL
    AND
    final_score IS NOT NULL
    AND
    assignment_avg IS NOT NULL
    AND
    quizzes_avg IS NOT NULL
    AND
    participation_score IS NOT NULL
    AND
    project_score IS NOT NULL
    AND
    total_score IS NOT NULL
    AND
    grade IS NOT NULL
    AND
    study_hours_per_week IS NOT NULL
    AND
    extracurricular_activities IS NOT NULL 
    AND
    internet_access_at_home IS NOT NULL 
    AND
    parent_education_level IS NOT NULL
    AND
    family_income_level IS NOT NULL
    AND
    stress_level IS NOT NULL
    AND
    sleep_hours_per_night IS NOT NULL ;

-- Creating student_data_invalid table

CREATE TABLE student_data_invalid as
SELECT * 
FROM student_data
WHERE
    student_id IS NULL
    OR 
    first_name IS NULL
    OR 
    last_name IS NULL
    OR
    email IS NULL
    OR
    gender IS NULL
    OR
    age IS NULL
    OR
    department IS NULL
    OR
    attendance IS NULL
    OR
    midterm_score IS NULL
    OR
    final_score IS NULL
    OR
    assignment_avg IS NULL
    OR
    quizzes_avg IS NULL
    OR
    participation_score IS NULL
    OR
    project_score IS NULL
    OR
    total_score IS NULL
    OR
    grade IS NULL
    OR
    study_hours_per_week IS NULL
    OR
    extracurricular_activities IS NULL 
    OR
    internet_access_at_home IS NULL 
    OR
    parent_education_level IS NULL
    OR
    family_income_level IS NULL
    OR
    stress_level IS NULL
    OR
    sleep_hours_per_night IS NULL ;

```
