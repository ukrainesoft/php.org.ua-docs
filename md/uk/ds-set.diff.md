---
navigation:
  - ds-set.count.md: '« Ds\\Set::count'
  - ds-set.filter.md: 'Ds\\Set::filter »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::diff'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::diff

(PECL ds >= 1.0.0)

Ds\\Set::diff — Створює новий набір з елементами, яких немає в іншому наборі

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

Новий набір, що містить всі елементи, які є в поточному наборі і відсутні в переданому `set`

### Дивіться також

-   [» Різниця множин](https://en.wikipedia.org/wiki/Complement_(set_theory))на Вікіпедія

### Приклади

**Приклад #1 Приклад використання**Ds\\Set::diff()\*\*\*\*

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->diff($b));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#3 (2) {
  [0]=>
  int(1)
  [1]=>
  int(2)
}
```
