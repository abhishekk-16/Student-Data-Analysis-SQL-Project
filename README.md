# Student-Data-Analysis-SQL-Project

## PROJECT OVERVIEW:

This project is designed to demonstrate SQL skills and techniques typically used by data analysts to explore, clean, and analyse student data. The project involves setting up a student database, performing exploratory data analysis (EDA), and answering specific questions through SQL queries. 

## OBJECTIVES:

1. **Set up a student database**: Creating and populating a student database with the provided student data.
2. **Data cleaning**: Identifying and removing any records with missing or null values.
3. **Exploratory Data Analysis (EDA)**: Performing basic EDA to understand the dataset.
4. **Data Analysis**: using SQL to answer specific questions and derive insights from the student data.

## PROJECT STRUCTURE:

## 1. Database Setup

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
