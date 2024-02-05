---
navigation:
  - ds-sequence.apply.md: '« Ds\\Sequence::apply'
  - ds-sequence.contains.md: 'Ds\\Sequence::contains »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::capacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::capacity

(PECL ds >= 1.0.0)

Ds\\Sequence::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
abstract public Ds\Sequence::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Пример #1 Пример использования**Ds\\Sequence::capacity()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector();
var_dump($sequence->capacity());

$sequence->push(...range(1, 50));
var_dump($sequence->capacity());

$sequence[] = "a";
var_dump($sequence->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(10)
int(50)
int(75)
```
