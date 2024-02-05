---
navigation:
  - ds-sequence.remove.md: '« Ds\\Sequence::remove'
  - ds-sequence.reversed.md: 'Ds\\Sequence::reversed »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::reverse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::reverse

(PECL ds >= 1.0.0)

Ds\\Sequence::reverse — Перевертає поточну колекцію

### Опис

```methodsynopsis
abstract public Ds\Sequence::reverse(): void
```

Перевертає поточну колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::reverse()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);
$sequence->reverse();

print_r($sequence);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => c
    [1] => b
    [2] => a
)
```
