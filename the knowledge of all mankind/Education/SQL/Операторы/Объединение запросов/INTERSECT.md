---
title: INTERSECT
date: 2024-07-18
tags:
  - программирование
  - обучение
---

## Описание
Оператор `INTERSECT` похож на оператор `UNION`. Он комбинирует два запроса `SELECT`, но возвращает только те строки, которые присутствуют в обоих результатах подзапросов.

Пример:
```sql
-- Найти студентов, которые записаны на курсы 'Mathematics' и 'Physics'
SELECT student_id
FROM enrollments
WHERE course_name = 'Mathematics'
INTERSECT
SELECT student_id
FROM enrollments
WHERE course_name = 'Physics';
```

## Ссылки
- [[UNION]]
