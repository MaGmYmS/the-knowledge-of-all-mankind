---
title: MIN
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Агрегатная функция `MIN` подсчитывает минимальное значение в атрибуте (колонке).

```sql
SELECT home_type, MIN(price) as avg_price FROM Rooms
GROUP BY home_type
```

## Ссылки
- [[Агрегатные функции]]
- [[Функции]]
