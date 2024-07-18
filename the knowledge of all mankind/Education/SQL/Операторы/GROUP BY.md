---
title: GROUP BY
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Оператор `GROUP BY` используется для группировки записей по определенному атрибуту. 

Синтаксис:
```sql
SELECT [литералы, агрегатные_функции, поля_группировки]
FROM имя_таблицы
GROUP BY поля_группировки;
```

Пример:
```sql
SELECT home_type, "literal" FROM Rooms
GROUP BY home_type
```

Так же, оператор `GROUP BY` нужен для работы агрегатные функции.  

```sql
SELECT home_type, AVG(price) as avg_price FROM Rooms
GROUP BY home_type
```

## Ссылки
- [[SELECT]]
- [[Агрегатные функции]]
- [[Порядок выполнения SQL запроса]]
