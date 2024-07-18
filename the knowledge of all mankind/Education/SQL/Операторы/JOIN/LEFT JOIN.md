---
title: LEFT JOIN
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Соединение, которое возвращает все значения из левой таблицы, соединённые с соответствующими значениями из правой таблицы, если они удовлетворяют условию соединения, или заменяет их на `NULL` в обратном случае.

Пример:
```sql
SELECT Timepair.id 'timepair.id', start_pair, end_pair,
    Schedule.id 'schedule.id', date, class, number_pair, teacher, subject, classroom
FROM Timepair
    LEFT JOIN Schedule ON Schedule.number_pair = Timepair.id;
```

## Ссылки
- [[OUTER JOIN]]
