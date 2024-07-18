---
title: HAVING
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Оператор `HAVING` используется для фильтрации групп (`GROUP BY`). Оператор `WHERE` в данном случае выдаст ошибку, поскольку выполняется раньше `GROUP BY`.

Синтаксис:
```sql
SELECT [константы, агрегатные_функции, поля_группировки]
FROM имя_таблицы
WHERE условия_на_ограничения_строк
GROUP BY поля_группировки
HAVING условие_на_ограничение_строк_после_группировки
ORDER BY условие_сортировки
```

Пример:
```sql
SELECT home_type, AVG(price) as avg_price FROM Rooms
GROUP BY home_type
HAVING avg_price > 50
```

```sql
SELECT home_type, MIN(price) as min_price FROM Rooms
WHERE has_tv = True
GROUP BY home_type
HAVING COUNT(*) >= 5;
```

## Ссылки
- [[SELECT]]
- [[GROUP BY]]
- [[WHERE]]
- [[Порядок выполнения SQL запроса]]
