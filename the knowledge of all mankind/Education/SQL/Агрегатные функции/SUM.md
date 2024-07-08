---
title: SUM
date: 2024-07-08
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Агрегатная функция `SUM` подсчитывает сумму значений в атрибуте (колонке).

```sql
SELECT home_type, SUM(price) as avg_price FROM Rooms
GROUP BY home_type
```

## Ссылки
- [[Агрегатные функции]]
- [[Функции]]
