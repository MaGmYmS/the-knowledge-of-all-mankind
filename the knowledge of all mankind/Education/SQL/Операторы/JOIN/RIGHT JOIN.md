---
title: LEFT JOIN
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Соединение, которое возвращает все значения из правой таблицы, соединённые с соответствующими значениями из левой таблицы, если они удовлетворяют условию соединения, или заменяет их на `NULL` в обратном случае.

Пример:
```sql
SELECT Timepair.id 'timepair.id', start_pair, end_pair,
    Schedule.id 'schedule.id', date, class, number_pair, teacher, subject, classroom
FROM Timepair RIGHT JOIN Schedule 
	ON Timepair.id = Schedule.number_pair;
```

## Ссылки
- [[OUTER JOIN]]
