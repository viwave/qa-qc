# Functional test cases:
- [ ] (добавить примеры)

# UI test cases:
- [ ] (добавить примеры)


---

## SQL база данных (SQLite)

Для примера была создана база SQLite как самое простое решение для визуализации домашнего задания.  
Написан запрос миграций и применён.

### Миграции
[migrate.sql](migrate.sql)

### Сиды
[seed.sql](seed.sql)

### SQL query
```sql
SELECT
    s.student_id,
    s.first_name,
    s.last_name,
    s.middle_name,
    s.address,
    g.group_name
FROM students s
         LEFT JOIN groups g
                   ON s.group_id = g.group_id
ORDER BY s.student_id ASC
LIMIT 10;
```
### Результат SQL query
![img.png](img.png)