---
navigation:
  - gender-gender.isnick.md: '« Gender\\Gender::isNick'
  - book.gettext.md: Gettext »
  - index.md: PHP Manual
  - class.gender.md: Gender\\Gender
title: 'Gender\\Gender::similarNames'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gender\\Gender::similarNames

(PECL gender >= 0.9.0)

Gender\\Gender::similarNames — Отримати схожі імена

### Опис

```methodsynopsis
public Gender\Gender::similarNames(string $name, int $country = ?): array
```

Отримати схожі імена для заданих імені та країни.

### Список параметрів

`name`

Ім'я для перевірки.

`country`

Ідентифікатор країни заданий константою класу. Якщо опущений, то використовується ANY\_COUNTRY.

### Значення, що повертаються

Повертає масив із знайденими схожими іменами.
