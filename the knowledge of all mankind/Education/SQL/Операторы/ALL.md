---
title: ALL
date: 2024-07-18
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Условное выражение с `ALL` возвращает `TRUE`, если все сравнения отдельного значения со значением в наборе вернут `TRUE`.

Например, нижеприведённый синтетический запрос проверяет для всех ли жилых помещений выполняется условие, что оно дешевле чем 200:
```sql
SELECT 200 > ALL(SELECT price FROM Rooms)
```

## Ссылки
- [[SELECT]]
- [[Подзапросы с несколькими строками и одним столбцом]]
