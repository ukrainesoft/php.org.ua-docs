---
navigation:
  - gender-gender.isnick.html: '« GenderGender::isNick'
  - book.gettext.md: Gettext »
  - index.md: PHP Manual
  - class.gender.md: GenderGender
title: 'GenderGender::similarNames'
---
# GenderGender::similarNames

(PECL gender >= 0.9.0)

GenderGender::similarNames — Отримати схожі імена

### Опис

```methodsynopsis
public Gender\Gender::similarNames(string $name, int $country = ?): array
```

Отримати схожі імена для заданих імені та країни.

### Список параметрів

`name`

Ім'я для перевірки.

`country`

Ідентифікатор країни заданий константою класу. Якщо опущений, то використовується ANYCOUNTRY.

### Значення, що повертаються

Повертає масив із знайденими схожими іменами.
