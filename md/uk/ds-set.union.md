---
navigation:
  - ds-set.toarray.md: '« Ds\\Set::toArray'
  - ds-set.xor.md: 'Ds\\Set::xor »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::union'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::union

(PECL ds >= 1.0.0)

Ds\\Set::union — Створення нового набору з елементів поточного та переданого наборів

### Опис

```methodsynopsis
public Ds\Set::union(Ds\Set $set): Ds\Set
```

Створює новий набір з елементів поточного та переданого в `set`наборов.

`A ∪ B = {x: x ∈ A ∨ x ∈ B}`

### Список параметрів

`set`

Новий набір для об'єднання із поточним.

### Значення, що повертаються

Новий набір, що є об'єднанням поточного та переданого в `set`

### Дивіться також

-   [» Об'єднання](https://en.wikipedia.org/wiki/Union_(set_theory))в Вікіпедія

### Приклади

**Приклад #1 Приклад використання** Ds\\Set::union()\*\*\*\*

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->union($b));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#3 (5) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  int(4)
  [4]=>
  int(5)
}
```
