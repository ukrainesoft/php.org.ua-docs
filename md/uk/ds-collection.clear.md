---
navigation:
  - class.ds-collection.md: « Ds\\Collection
  - ds-collection.copy.md: 'Ds\\Collection::copy »'
  - index.md: PHP Manual
  - class.ds-collection.md: Ds\\Collection
title: 'Ds\\Collection::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Collection::clear

(PECL ds >= 1.0.0)

Ds\\Collection::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\Collection::clear(): void
```

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример**Ds\\Collection::clear()\*\*\*\*

```php
<?php
$collection = new \Ds\Vector([1, 2, 3]);
print_r($collection);

$collection->clear();
print_r($collection);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Vector Object
(
)
```
