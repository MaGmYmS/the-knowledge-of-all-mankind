---
title: ORDER BY
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Оператор `ORDER BY` используется для сортировки записей по двум правилам:
- `ASC` - сортировка по возрастанию (по умолчанию)
- `DESC` - сортировка по убыванию

Синтаксис:
```sql
SELECT поля_таблиц FROM наименование_таблицы
WHERE ...
ORDER BY столбец_1 [ASC | DESC][, столбец_n [ASC | DESC]]
```

Пример:
```sql
SELECT name FROM Company ORDER BY name;
```

```sql
SELECT DISTINCT town_from, town_to FROM Trip
ORDER BY town_from DESC, town_to DESC;
```

## Ссылки
- [[SELECT]]
- [[Порядок выполнения SQL запроса]]
