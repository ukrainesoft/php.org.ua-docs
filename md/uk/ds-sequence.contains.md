---
navigation:
  - ds-sequence.capacity.md: '« Ds\\Sequence::capacity'
  - ds-sequence.filter.md: 'Ds\\Sequence::filter »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::contains'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::contains

(PECL ds >= 1.0.0)

Ds\\Sequence::contains — Перевіряє, чи містяться в колекції задані значення

### Опис

```methodsynopsis
abstract public Ds\Sequence::contains(mixed ...$values): bool
```

Перевіряє, чи містяться у колекції задані значення.

### Список параметрів

`values`

Значення для перевірки.

### Значення, що повертаються

Повертає \*\*`false`\*\*якщо хоча б одне значення з `values` не знайдено в колекції та **`true`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::contains()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(['a', 'b', 'c', 1, 2, 3]);

var_dump($sequence->contains('a'));                // true
var_dump($sequence->contains('a', 'b'));           // true
var_dump($sequence->contains('c', 'd'));           // false

var_dump($sequence->contains(...['c', 'b', 'a'])); // true

// Всегда строгая проверка
var_dump($sequence->contains(1));                  // true
var_dump($sequence->contains('1'));                // false

var_dump($sequece->contains(...[]));               // true
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
bool(false)
bool(true)
bool(true)
bool(false)
bool(true)
```
