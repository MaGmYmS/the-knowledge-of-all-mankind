---
title: DISTINCT
date: 2024-07-07
tags:
  - программирование
  - обучение
  - SQL
---

## Описание
Оператор `DISTINCT` используется для получения уникальных значений из поля.

```sql
SELECT DISTINCT class FROM Student_in_class;
```

При использовании оператора `DISTINCT` для двух и более колонок будут удаляться записи, которые имеют одинаковые значения по всем полям.
```sql
SELECT DISTINCT first_name, last_name FROM User;
```

## Ссылки
- [[SELECT]]
