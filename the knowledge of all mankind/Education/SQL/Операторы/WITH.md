---
title: WITH
date: 2024-07-18
tags:
  - программирование
  - обучение
---

## Описание
Обобщённое табличное выражение или CTE (Common Table Expressions) - это временный результирующий набор данных, к которому можно обращаться в последующих запросах. Для написания обобщённого табличного выражения используется оператор `WITH`.

Синтаксис:
```sql
WITH название_cte [(столбец_1 [, столбец_2 ] …)] AS (подзапрос)
    [, название_cte [(столбец_1 [, столбец_2 ] …)] AS (подзапрос)] …
```

Пример:
```sql
WITH Aeroflot_trips (aeroflot_plane, town_from, town_to) AS
    (SELECT plane, town_from, town_to FROM Company
        INNER JOIN Trip ON Trip.company = Company.id WHERE name = "Aeroflot")

SELECT * FROM Aeroflot_trips;
```

С помощью оператора `WITH` определяем несколько табличных выражений:
```sql
WITH Aeroflot_trips AS
    (SELECT TRIP.* FROM Company
        INNER JOIN Trip ON Trip.company = Company.id WHERE name = "Aeroflot"),
    Don_avia_trips AS
    (SELECT TRIP.* FROM Company
        INNER JOIN Trip ON Trip.company = Company.id WHERE name = "Don_avia")

SELECT * FROM Don_avia_trips UNION SELECT * FROM  Aeroflot_trips;
```

Выражение с `WITH` считается «временным», потому что результат не сохраняется где-либо на постоянной основе в схеме базы данных, а действует как временное представление, которое существует только на время выполнения запроса, то есть оно доступно только во время выполнения операторов `SELECT`, `INSERT`, `UPDATE`, `DELETE` или `MERGE`. Оно действительно только в том запросе, которому он принадлежит, что позволяет улучшить структуру запроса, не загрязняя глобальное пространство имён.
## Ссылки
- [[SELECT]]
