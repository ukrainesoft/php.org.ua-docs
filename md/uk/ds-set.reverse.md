---
navigation:
  - ds-set.remove.md: '« Ds\\Set::remove'
  - ds-set.reversed.md: 'Ds\\Set::reversed »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::reverse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::reverse

(PECL ds >= 1.0.0)

Ds\\Set::reverse — Перевертає поточну колекцію

### Опис

```methodsynopsis
public Ds\Set::reverse(): void
```

Перевертає поточну колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Set::reverse()\*\*\*\*

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);
$set->reverse();

print_r($set);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Set Object
(
    [0] => c
    [1] => b
    [2] => a
)
```
