---
navigation:
  - gender-gender.get.md: '« Gender\\Gender::get'
  - gender-gender.similarnames.md: 'Gender\\Gender::similarNames »'
  - index.md: PHP Manual
  - class.gender.md: Gender\\Gender
title: 'Gender\\Gender::isNick'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gender\\Gender::isNick

(PECL gender >= 0.9.0)

Gender\\Gender::isNick — Перевіряє, чи є name0 псевдонімом для name1

### Опис

```methodsynopsis
public Gender\Gender::isNick(string $name0, string $name1, int $country = ?): array
```

Перевіряє, чи name0 є псевдонімом для name1.

### Список параметрів

`name0`

Ім'я для перевірки.

`name1`

Ім'я для перевірки.

`country`

Ідентифікатор країни, яка визначається константою класу Gender. Якщо опущений, то використовується ANY\_COUNTRY.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
