---
title: Многотабличные запросы
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Чтобы связать несколько таблиц в одну, используется оператор `JOIN`.

Структура многотабличного запроса:
```sql
SELECT поля_таблиц
FROM таблица_1
[INNER] | [[LEFT | RIGHT | FULL][OUTER]] JOIN таблица_2
    ON условие_соединения
[[INNER] | [[LEFT | RIGHT | FULL][OUTER]] JOIN таблица_n
    ON условие_соединения]
```

Как можно увидеть по структуре, соединение бывает:

- внутренним `INNER` (по умолчанию).
- внешним `OUTER`, при этом внешнее соединение делится на левое `LEFT`, правое `RIGHT` и полное `FULL`.

Пример:
```sql
SELECT family_member, member_name, amount * unit_price AS price FROM Payments
INNER JOIN FamilyMembers
    ON Payments.family_member = FamilyMembers.member_id
```

При необходимости вывести все строки из таблицы, можно использовать символ `*`:
```sql
SELECT FamilyMembers.* FROM Payments
INNER JOIN FamilyMembers
    ON Payments.family_member = FamilyMembers.member_id
```

Для нескольких таблиц:
```sql
SELECT Payments.*, FamilyMembers.* FROM Payments
INNER JOIN FamilyMembers
    ON Payments.family_member = FamilyMembers.member_id
```

Все возможные варианты `JOIN`:

| Схема                                                                                     | Запрос с JOIN                                                                                                                                |
| ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| ![](https://sql-academy.org/static/guidePage/multi-table-request-join/left.svg)           | Получение всех данных из левой таблицы, соединённых с соответствующими данными из правой:<br><br>![[Pasted image 20240708124400.png]]        |
| ![](https://sql-academy.org/static/guidePage/multi-table-request-join/right.svg)          | Получение всех данных из правой таблицы, соединённых с соответствующими данными из левой:<br><br>![[Pasted image 20240708124445.png]]        |
| ![](https://sql-academy.org/static/guidePage/multi-table-request-join/left_no_right.svg)  | Получение данных, относящихся только к левой таблице:<br><br>![[Pasted image 20240708124502.png]]                                            |
| ![](https://sql-academy.org/static/guidePage/multi-table-request-join/right_no_left.svg)  | Получение данных, относящихся только к правой таблице:<br><br>![[Pasted image 20240708124518.png]]                                           |
| ![](https://sql-academy.org/static/guidePage/multi-table-request-join/right_and_left.svg) | Получение данных, относящихся как к левой, так и к правой таблице:<br><br>![[Pasted image 20240708124533.png]]                               |
| ![](https://sql-academy.org/static/guidePage/multi-table-request-join/all.svg)            | Получение всех данных, относящихся к левой и правой таблицам, а также их внутреннему соединению:<br><br>![[Pasted image 20240708124547.png]] |
| ![](https://sql-academy.org/static/guidePage/multi-table-request-join/right_xor_left.svg) | Получение данных, не относящихся к левой и правой таблицам одновременно (обратное INNER JOIN):<br><br>![[Pasted image 20240708124637.png]]   |

## Ссылки
- [[SELECT]]
- [[INNER JOIN]]
- [[OUTER JOIN]]
