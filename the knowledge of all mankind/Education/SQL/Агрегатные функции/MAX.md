---
title: MAX
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Агрегатная функция `MAX` подсчитывает максимальное значение в атрибуте (колонке).

```sql
SELECT home_type, MAX(price) as avg_price FROM Rooms
GROUP BY home_type
```

## Ссылки
- [[Агрегатные функции]]
- [[Функции]]
