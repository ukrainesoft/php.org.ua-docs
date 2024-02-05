---
navigation:
  - ds-sequence.last.md: '« Ds\\Sequence::last'
  - ds-sequence.merge.md: 'Ds\\Sequence::merge »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::map'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::map

(PECL ds >= 1.0.0)

Ds\\Sequence::map — Повертає результат застосування callback-функції до всіх значень колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::map(callable $callback): Ds\Sequence
```

Повертає результат застосування callback-функції, переданої в `callback`до всіх значень колекції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Аргумент типа[callable](language.types.callable.md)

Ця функція повинна повертати нове значення для кожного елемента колекції.

### Значення, що повертаються

Результат применения`callback` до кожного значення колекції.

> **Зауваження** :
> 
> Значення поточної колекції залишаться незмінними.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::map()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

print_r($sequence->map(function($value) { return $value * 2; }));
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
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
```
