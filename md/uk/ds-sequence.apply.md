---
navigation:
  - ds-sequence.allocate.md: '« Ds\\Sequence::allocate'
  - ds-sequence.capacity.md: 'Ds\\Sequence::capacity »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::apply'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::apply

(PECL ds >= 1.0.0)

Ds\\Sequence::apply — Оновлення всіх значень застосуванням до них переданої callback-функції

### Опис

```methodsynopsis
abstract public Ds\Sequence::apply(callable $callback): void
```

Оновлення всіх значень застосуванням до них переданої `callback`\-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Об'єкт типу [callable](language.types.callable.md)

Callback-функція має повертати нове значення, яке замінить поточне.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::apply()\*\*\*\*

```php
<?php
$sequence = new \Ds\Sequence([1, 2, 3]);
$sequence->apply(function($value) { return $value * 2; });

print_r($sequence);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
```
