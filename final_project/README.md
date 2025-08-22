# Functional test cases:
- [ ] (добавить примеры)

# UI test cases:
- [ ] (добавить примеры)


---

## SQL база данных (SQLite)

Для примера была создана база SQLite как самое простое решение для визуализации домашнего задания.  
Написан запрос миграций и применён.

### Миграции

```sql
CREATE TABLE faculties
(
   faculty_id   INT PRIMARY KEY,
   faculty_name VARCHAR(100)
);

CREATE TABLE departments
(
   department_id   INT PRIMARY KEY,
   department_name VARCHAR(100),
   faculty_id      INT,
   FOREIGN KEY (faculty_id) REFERENCES faculties (faculty_id)
);

CREATE TABLE groups
(
   group_id      INT PRIMARY KEY,
   group_name    VARCHAR(50),
   department_id INT,
   FOREIGN KEY (department_id) REFERENCES departments (department_id)
);

CREATE TABLE students
(
   student_id  INT PRIMARY KEY,
   first_name  VARCHAR(50),
   last_name   VARCHAR(50),
   middle_name VARCHAR(50),
   address     VARCHAR(255),
   group_id    INT,
   FOREIGN KEY (group_id) REFERENCES groups (group_id)
);
