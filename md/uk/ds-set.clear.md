---
navigation:
  - ds-set.capacity.md: '« Ds\\Set::capacity'
  - ds-set.construct.md: 'Ds\\Set::\_\_construct »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::clear

(PECL ds >= 1.0.0)

Ds\\Set::clear — Видаляє всі значення з колекції

### Опис

```methodsynopsis
public Ds\Set::clear(): void
```

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Set::clear()\*\*\*\*

```php
<?php
$set = new \Ds\Set([1, 2, 3]);
print_r($set);

$set->clear();
print_r($set);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Set Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Set Object
(
)
```
