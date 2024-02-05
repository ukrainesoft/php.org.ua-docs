---
navigation:
  - ds-sequence.filter.md: '« Ds\\Sequence::filter'
  - ds-sequence.first.md: 'Ds\\Sequence::first »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::find'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::find

(PECL ds >= 1.0.0)

Ds\\Sequence::find — Пошук індексу за значенням

### Опис

```methodsynopsis
abstract public Ds\Sequence::find(mixed $value): mixed
```

Повертає індекс значення `value`, или\*\*`false`\*\*якщо нічого не знайдено.

### Список параметрів

`value`

Шукане значення.

### Значення, що повертаються

Індекс елемента, або \*\*`false`\*\*якщо значення не знайдено.

> **Зауваження** :
> 
> Елементи порівнюються строго, за типом та значенням.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::find()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", 1, true]);

var_dump($sequence->find("a")); // 0
var_dump($sequence->find("b")); // false
var_dump($sequence->find("1")); // false
var_dump($sequence->find(1));   // 1
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(0)
bool(false)
bool(false)
int(1)
```
