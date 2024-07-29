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

Después de pensarlo, la solución más acorde con un escenario real (aunque no la única), me parece que sería:
- cada course está asociado a un único professor
- cada student se matricula en varios courses
- cada grade se asocia a un course, y a un alumno
de esta manera, al generar cada result de grade, se asignaría a cada uno de los courses que haga el student


## Creamos una base de datos con las siguientes tablas: Students, Courses, Professors, Grades.
Dentro de cada una, creo las siguientes columnas:

#### Students
 * student_id INT Clave primaria, Obligatoria, Única y Autoincremental
 * student_name VARCHAR(100) Obligatoria
 * student_email VARCHAR(100)
  ```
  CREATE TABLE `students` (
    `student_id` int NOT NULL AUTO_INCREMENT,
    `student_name` varchar(100) NOT NULL,
    `student_mail` varchar(100) DEFAULT NULL,
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
 * professor_name VARCHAR(100) Obligatoria
 * professor_email VARCHAR(100) 
  ```
  CREATE TABLE `professors` (
    `professor_id` int NOT NULL AUTO_INCREMENT,
    `professor_name` varchar(45) NOT NULL,
    `professor_mail` varchar(45) DEFAULT NULL,
    PRIMARY KEY (`professor_id`),
    UNIQUE KEY `professor_id_UNIQUE` (`professor_id`)
  ```
---
## Crea claves foráneas para relacionar las tablas entre sí.

> cada `professor` está asociado a un `course` siendo este el que imparte

> Las claves foráneas las he creado dentro de la tabla `grades`, así cada calificación apuntará a un `student`, y a un `course`

> Luego, la nota va en `grade_result`, siendo esta decimal

> Además cada `course` apunta a un único `professor`

#### Grades 
 * grade_id INT Clave primaria, Obligatoria, Única y Autoincremental
 * grade_result Decimal (2,2) Obligatoria
 * grade_student_id INT
 * grade_course_id INT

  ```
  CREATE TABLE `grades` (
  `grade_id` int NOT NULL AUTO_INCREMENT,
  `grade_student_id` int NOT NULL,
  `grade_course_id` int NOT NULL,
  `grade_result` decimal(2,2) NOT NULL,
  PRIMARY KEY (`grade_id`),
  UNIQUE KEY `grade_id_UNIQUE` (`grade_id`),
  KEY `grade_student_id_idx` (`grade_student_id`),
  KEY `grade_course_id_idx` (`grade_course_id`),
  KEY `grade_professor_id_idx` (`grade_professor_id`),
  CONSTRAINT `grade_course_id` FOREIGN KEY (`grade_course_id`) REFERENCES `courses` (`course_id`) ON DELETE CASCADE,
  CONSTRAINT `grade_student_id` FOREIGN KEY (`grade_student_id`) REFERENCES `students` (`student_id`) ON DELETE CASCADE
  ```

#### Course
 *  course_professor_id INT 

'KEY `course_professor_id_idx` (`course_professor_id`)'

---
## Crea un script que rellene todas las tablas con datos de ejemplo.

`USE sql_university_project;`
```
INSERT INTO students(student_name, student_email)
VALUES ("Pepe Gonzalez", 'pepegonzalez@gmail.com');

INSERT INTO students(student_name, student_email)
VALUES ("Maria Fernandez", 'mariafernandez@gmail.com');

INSERT INTO students(student_name, student_email)
VALUES ("Felipe Gomez", 'felipegomez@gmail.com');

INSERT INTO students(student_name, student_email)
VALUES ("Clara Lopez", 'claralopez@gmail.com');
```
```
INSERT INTO courses(course_name, course_professor_id)
VALUES ("matemáticas", 1);

INSERT INTO courses(course_name, course_professor_id)
VALUES ("física", 2);

INSERT INTO courses(course_name, course_professor_id)
VALUES ("inglés", 3);

INSERT INTO courses(course_name, course_professor_id)
VALUES ("gramática", 9 );
```
```
INSERT INTO professors(professor_name, professor_email)
VALUES ("Sr Ramirez", 'sr_ramirez@gmail.com');

INSERT INTO professors(professor_name, professor_email)
VALUES ("Sr Guzman", 'sr_guzman@gmail.com');

INSERT INTO professors(professor_name, professor_email)
VALUES ("Sra Sanchez", 'sra_sanchez@gmail.com');

INSERT INTO professors(professor_name, professor_email)
VALUES ("Sra Perez", 'sra_perez@gmail.com');
```
> Después creo, como si se hubiese ido introduciendo, cada calificación asociada a cada estudiante y cada asignatura

```
INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (1, 1, 8.5);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (1, 2, 9.5);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (1, 3, 7.0);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (1, 4, 6.8);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (2, 1, 8.5);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (2, 2, 9.0);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (2, 3, 9.8);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (3, 3, 4.8);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (3, 4, 6.0);

INSERT INTO grades(grade_student_id, grade_course_id, grade_result)
VALUES  (4, 3, 7.5);

```
---
## Crea scripts de consulta SQL para:

### La nota media que da cada profesor.
```
SELECT
    p.professor_name AS PROFESOR,
    cast(AVG (g.grade_result) as dec(4,2)) AS NOTA_MEDIA
FROM grades g
JOIN professors p 
	ON g.grade_course_id = p.professor_id
GROUP BY g.grade_course_id;
```
|PROFESOR| NOTA_MEDIA
|------------|--------
|Sra Sanchez| 7.28
|Sra Perez| 6.40
|Sr Ramirez| 8.50
|Sr Guzman| 9.25

> Para este script, He buscado información y he modificado el average de int a decimal con un `cast` para evitar que esta media la diese con demasiados decimales. 
Luego, no tenía claro si es muy ortodoxo, pero el condicional, es igualar un course_id con un professor_id, esto funciona porque pensé que lo más lógigo sería que cada profesor impartiese una sola asignatura, así que su id con el de esta coinciden.
---
### Las mejores notas de cada estudiante.
```
SELECT 
    s.student_name AS ALUMNO,
    MAX (g.grade_result) AS MEJOR_NOTA
FROM grades g
JOIN students s 
	ON g.grade_student_id = s.student_id;
```
|ALUMNO	|MEJOR_NOTA
|--------------|----
|Pepe Gonzalez	|9.50
|Maria Fernandez	|9.80
|Felipe Gomez	|6.00
|Clara Lopez	|7.50

---
### Ordenar a los estudiantes por los cursos en los que están matriculados.
```
SELECT
    s.student_name AS ALUMNO,
    c.course_name AS CURSO
FROM grades g
JOIN students s 
	ON g.grade_student_id = s.student_id
JOIN courses c 
	ON g.grade_course_id = c.course_id
ORDER BY g.grade_student_id ASC;
```
|ALUMNO|	CURSO
|-------------|-------------
|Pepe Gonzalez	|matemáticas
|Pepe Gonzalez	|física
|Pepe Gonzalez	|inglés
|Pepe Gonzalez	|gramática
|Maria Fernandez	|matemáticas
|Maria Fernandez	|física
|Maria Fernandez	|inglés
|Felipe Gomez	|inglés
|Felipe Gomez	|gramática
|Clara Lopez	|inglés
---
### Crear un informe resumido de los cursos y sus notas medias, ordenados desde el curso más difícil (curso con la nota media más baja) hasta el curso más fácil.

```
SELECT
    c.course_name AS CURSO,
    cast(AVG (g.grade_result) as dec(2,2)) AS NOTA_MEDIA
FROM grades g
JOIN courses c 
	ON g.grade_course_id = c.course_id
GROUP BY g.grade_course_id
ORDER BY NOTA_MEDIA ASC;
```
|CURSO| NOTA_MEDIA
|-----------|--------
|gramática| 6.40
|inglés| 7.28
|matemáticas| 8.50
|física| 9.25

> Para este script, He buscado información y he modificado el average de int a decimal con un `cast` para evitar que esta media la diese con demasiados decimales. 
Luego he utilizado el alias del average para ordenar la lista de más difícil a más fácil
---
### Encontrar qué estudiante y profesor tienen más cursos en común.
> Por el planteamiento, cada case tiene asignada un único profesor, así que he desarrollado el script de igual manera, pero el resultado siempre es `1`
```
SELECT
	s.student_name AS ALUMNO,
	p.professor_name AS PROFESOR,
    COUNT(g.grade_id) AS NUMERO_CURSOS
FROM grades g
JOIN courses c
 ON c.course_id = g.grade_course_id 
JOIN students s
	ON s.student_id = g.grade_student_id    
JOIN professors p
	 ON p.professor_id = g.grade_course_id
GROUP BY s.student_name, p.professor_name
```
|ALUMNO	|PROFESOR|	NUMERO_CURSOS
|-------------|------------|------------
|Pepe Gonzalez	|Sr Ramirez	|1
|Pepe Gonzalez	|Sr Guzman	|1
|Pepe Gonzalez	|Sra Sanchez	|1
|Pepe Gonzalez	|Sra Perez	|1
|Maria Fernandez	|Sr Ramirez	|1
|Maria Fernandez	|Sr Guzman	|1
|Maria Fernandez	|Sra Sanchez	|1
|Felipe Gomez	|Sra Sanchez	|1
|Felipe Gomez	|Sra Perez	|1
|Clara Lopez	|Sra Sanchez	|1

> Como alternativa, he creado un script para averiguar cuantos alumnos coinciden en un mismo curso:
