---
title: IN
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Оператор `IN` позволяет узнать входит ли проверяемое значение столбца в список определённых значений.

Пример:
```sql
SELECT * FROM FamilyMembers
WHERE status IN ('father', 'mother');
```

Пример с подзапросом:
```sql
SELECT * FROM Users WHERE id IN (
    SELECT DISTINCT owner_id FROM Rooms WHERE price >= 150
)
```
## Ссылки
- [[WHERE]]
- [[Подзапросы с несколькими строками и одним столбцом]]
