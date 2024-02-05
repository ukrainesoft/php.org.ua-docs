---
navigation:
  - ds-stack.clear.md: '« Ds\\Stack::clear'
  - ds-stack.copy.md: 'Ds\\Stack::copy »'
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::\_\_construct

(PECL ds >= 1.0.0)

Ds\\Stack::\_\_construct — Створює новий екземпляр класу

### Опис

public**Ds\\Stack::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `$values`

Створює новий екземпляр класу, використовуючи або об'єкт реалізує [traversable](class.traversable.md), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Пример #1 Пример использования**Ds\\Stack::\_\_construct()\*\*\*\*

```php
<?php
$stack = new \Ds\Stack();
print_r($stack);

$stack = new \Ds\Stack([1, 2, 3]);
print_r($stack);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Stack Object
(
)
Ds\Stack Object
(
    [0] => 3
    [1] => 2
    [2] => 1
)
```
