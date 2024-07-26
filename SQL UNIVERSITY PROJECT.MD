# Project Requirements for SQL Course

## Project Overview
> Build a SQL database for a university that manages students, courses, professors, and grades.

## Project Technical Requirements

### The project needs to contain the following technical features:
- Build a database with the following tables: `Students`, `Courses`, `Professors`, `Grades`
- Foreign key relationships between the tables
- Create a script that populates all of the database tables with sample data
- SQL query scripts for:
  * The average grade that is given by each professor
  * The top grades for each student
  * Sort students by the courses that they are enrolled in
  * Create a summary report of courses and their average grades, sorted by the most challenging course (course with the lowest average grade) to the easiest course
  * Finding which student and professor have the most courses in common
> #### Submission options: Push all scripts to a single Github repository and submit the link to a Mentor through the support app. If you're not familiar with Github, create a separate gist for all of the scripts and submit the gist through the support app.

---
---
> El proyecto necesita contener las siguientes características técnicas:

## Creamos una base de datos con las siguientes tablas: Students, Courses, Professors, Grades.
Dentro de cada una, creo las siguientes columnas:

#### Students
 * student_id INT Clave primaria, Obligatoria, Única y Autoincremental
 * student_name VARCHAR(45) Obligatoria
 * student_email VARCHAR(45)
  ```
  CREATE TABLE `students` (
    `student_id` int NOT NULL AUTO_INCREMENT,
    `student_name` varchar(45) NOT NULL,
    `student_mail` varchar(45) DEFAULT NULL,
    PRIMARY KEY (`student_id`),
    UNIQUE KEY `student_id_UNIQUE` (`student_id`)
  ```
#### Courses
 * course_id INT Clave primaria, Obligatoria, Única y Autoincremental
 * course_name VARCHAR(45) Obligatoria
  ```
  CREATE TABLE `courses` (
    `course_id` int NOT NULL AUTO_INCREMENT,
    `course_name` varchar(45) NOT NULL,
    PRIMARY KEY (`course_id`),
    UNIQUE KEY `course_id_UNIQUE` (`course_id`)
  ```
#### Professors
 * professor_id INT Clave primaria, Obligatoria, Única y Autoincremental
 * professor_name VARCHAR(45) Obligatoria
 * professor_email VARCHAR(45) 
  ```
  CREATE TABLE `professors` (
    `professor_id` int NOT NULL AUTO_INCREMENT,
    `professor_name` varchar(45) NOT NULL,
    `professor_mail` varchar(45) DEFAULT NULL,
    PRIMARY KEY (`professor_id`),
    UNIQUE KEY `professor_id_UNIQUE` (`professor_id`)
  ```
#### Grades 
* grade_id INT Clave primaria, Obligatoria, Única y Autoincremental



## Crea claves foráneas para relacionar las tablas entre sí.
## Crea un script que rellene todas las tablas con datos de ejemplo.
## Crea scripts de consulta SQL para:
  * La nota media que da cada profesor.
  * Las mejores notas de cada estudiante.
  * Ordenar a los estudiantes por los cursos en los que están matriculados.
  * Crear un informe resumido de los cursos y sus notas medias, ordenados desde el curso más difícil (curso con la nota media más baja) hasta el curso más fácil.
  * Encontrar qué estudiante y profesor tienen más cursos en común.
