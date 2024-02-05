---
navigation:
  - ds-sequence.reverse.md: '« Ds\\Sequence::reverse'
  - ds-sequence.rotate.md: 'Ds\\Sequence::rotate »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::reversed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::reversed

(PECL ds >= 1.0.0)

Ds\\Sequence::reversed — Повертає перегорнуту копію колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::reversed(): Ds\Sequence
```

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія колекції.

> **Зауваження** :
> 
> Поточна колекція не зміниться.

### Приклади

**Пример #1 Пример использования**Ds\\Sequence::reversed()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

print_r($sequence->reversed());
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
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
)
```
