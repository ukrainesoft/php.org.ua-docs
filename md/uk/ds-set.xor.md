---
navigation:
  - ds-set.union.md: '« Ds\\Set::union'
  - class.ds-stack.md: Ds\\Stack »
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::xor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::xor

(PECL ds >= 1.0.0)

Ds\\Set::xor — Створює новий набір із значень, які є в одному з наборів, але не в обох одночасно

### Опис

```methodsynopsis
public Ds\Set::xor(Ds\Set $set): Ds\Set
```

Створює новий набір з значень, які є в поточному наборі, або в заданому наборі в `set`але не в обох одночасно.

`A ⊖ B = {x : x ∈ (A \ B) ∪ (B \ A)}`

### Список параметрів

`set`

Другий набір.

### Значення, що повертаються

Новий набір із значень, які є в поточному наборі, або в наборі, заданому в `set`але не в обох одночасно.

### Дивіться також

-   [» Симетрична різниця](https://en.wikipedia.org/wiki/Symmetric_difference)в Вікіпедія

### Приклади

**Приклад #1 Приклад використання** Ds\\Set::xor()\*\*\*\*

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->xor($b));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#3 (4) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(4)
  [3]=>
  int(5)
}
```
