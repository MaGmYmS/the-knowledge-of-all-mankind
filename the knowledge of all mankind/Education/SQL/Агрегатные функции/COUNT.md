---
title: COUNT
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Агрегатная функция `COUNT` подсчитывает количество записей в таблице или в атрибуте (колонке).

```sql
SELECT home_type, COUNT(*) as amount FROM Rooms
GROUP BY home_type
ORDER BY amount DESC
```

## Ссылки
- [[Агрегатные функции]]
- [[Функции]]
