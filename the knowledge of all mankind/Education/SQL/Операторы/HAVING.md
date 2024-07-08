---
title: HAVING
date: 2024-07-08
tags:
  - программирование
  - обучение
---

## Описание
Оператор `HAVING` используется для фильтрации групп (`GROUP BY`). Оператор `WHERE` в данном случае выдаст ошибку, поскольку выполняется раньше `GROUP BY`.

```sql
SELECT home_type, AVG(price) as avg_price FROM Rooms
GROUP BY home_type
HAVING avg_price > 50
```

## Ссылки
- [[SELECT]]
- [[GROUP BY]]
- [[WHERE]]
- [[Порядок выполнения SQL запроса]]
