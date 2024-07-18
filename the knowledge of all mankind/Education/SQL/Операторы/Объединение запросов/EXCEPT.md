---
title: EXCEPT
date: 2024-07-18
tags:
  - программирование
  - обучение
---

## Описание
Оператор `EXCEPT` похож на оператор `UNION`. Он комбинирует два запроса `SELECT`, но возвращает строки, которые присутствуют в первом подзапросе, но отсутствуют во втором.

Пример:
```sql
-- Найти студентов, которые записаны на курс 'Mathematics', но не записаны на курс 'Physics'
SELECT student_id
FROM enrollments
WHERE course_name = 'Mathematics'
EXCEPT
SELECT student_id
FROM enrollments
WHERE course_name = 'Physics';
```

## Ссылки
- [[UNION]]
