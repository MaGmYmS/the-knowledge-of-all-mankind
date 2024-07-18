---
title: INNER JOIN
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Внутреннее соединение — соединение, при котором находятся пары записей из двух таблиц, удовлетворяющие условию соединения, тем самым образуя новую таблицу, содержащую объединенные поля из исходных таблиц.

Для наглядности это выглядит следующим образом:
![[Pasted image 20240708122925.png]]

Структура:
```sql
SELECT поля_таблиц
FROM таблица_1
[INNER] JOIN таблица_2
    ON условие_соединения
[[INNER] JOIN таблица_n
    ON условие_соединения]
```

Пример:
```sql
SELECT family_member, member_name FROM Payments
INNER JOIN FamilyMembers
    ON Payments.family_member = FamilyMembers.member_id
```

PS:
Так как, по умолчанию, если не указаны какие-либо параметры, `JOIN` выполняется как `INNER JOIN`, то при внутреннем соединении `INNER` является **опциональным**.

PPS:
Для внутреннего соединения таблиц также можно использовать оператор `WHERE`. Например, вышеприведённый запрос, написанный с помощью `INNER JOIN`, будет выглядеть так:
```sql
SELECT family_member, member_name FROM Payments, FamilyMembers
    WHERE Payments.family_member = FamilyMembers.member_id
```
## Ссылки
- [[JOIN]]
