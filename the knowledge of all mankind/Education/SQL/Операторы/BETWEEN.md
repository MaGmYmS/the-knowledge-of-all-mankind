---
title: BETWEEN
date: 2024-07-07
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Оператор `BETWEEN min AND max` позволяет узнать расположено ли проверяемое значение столбца в интервале между `min` и `max`, включая сами значения `min` и `max`.
```sql
SELECT * FROM Payments
WHERE unit_price BETWEEN 100 AND 500;
```

## Ссылки
- [[WHERE]]
