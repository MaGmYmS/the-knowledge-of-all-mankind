---
title: AVG
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Агрегатная функция `AVG` подсчитывает среднее значение в атрибуте (колонке).

```sql
SELECT home_type, AVG(price) as avg_price FROM Rooms
GROUP BY home_type
```

## Ссылки
- [[Агрегатные функции]]
- [[Функции]]
