---
navigation:
  - ds-set.count.md: '« DsSet::count'
  - ds-set.filter.md: 'ДсSet::filter »'
  - index.md: PHP Manual
  - class.ds-set.md: Набор
title: 'ДсSet::diff'
---
# ДсSet::diff

(PECL ds >= 1.0.0)

ДсSet::diff — Створює новий набір з елементами, яких немає в іншому наборі

### Опис

```methodsynopsis
public Ds\Set::diff(Ds\Set $set): Ds\Set
```

Створює новий набір із елементами, яких немає в іншому наборі.

`A \ B = {x ∈ A | x ∉ B}`

### Список параметрів

`set`

Набір містить елементи, які треба виключити з нового набору.

### Значення, що повертаються

Новий набір, що містить усі елементи, які є в поточному наборі та відсутні в переданому `set`

### Дивіться також

-   [» Різниця множин](https://en.wikipedia.org/wiki/Complement_(set_theory)) на Вікіпедія

### Приклади

**Приклад #1 Приклад використання**ДсSet::diff()\*\*\*\*

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->diff($b));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#3 (2) {
  [0]=>
  int(1)
  [1]=>
  int(2)
}
```
