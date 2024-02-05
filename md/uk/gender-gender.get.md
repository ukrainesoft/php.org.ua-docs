---
navigation:
  - gender-gender.country.md: '« Gender\\Gender::country'
  - gender-gender.isnick.md: 'Gender\\Gender::isNick »'
  - index.md: PHP Manual
  - class.gender.md: Gender\\Gender
title: 'Gender\\Gender::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gender\\Gender::get

(PECL gender >= 0.6.0)

Gender\\Gender::get — Отримати підлогу на ім'я

### Опис

```methodsynopsis
public Gender\Gender::get(string $name, int $country = ?): int
```

Отримати підлогу на ім'я в заданій країні.

### Список параметрів

`name`

Ім'я для перевірки.

`country`

Ідентифікатор країни заданий константою класу Gender.

### Значення, що повертаються

Повертає підлогу на ім'я.
