---
navigation:
  - gender-gender.country.md: '« GenderGender::country'
  - gender-gender.isnick.md: 'GenderGender::isNick »'
  - index.md: PHP Manual
  - class.gender.md: GenderGender
title: 'GenderGender::get'
---
# GenderGender::get

(PECL gender >= 0.6.0)

GenderGender::get — Отримати підлогу на ім'я

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
