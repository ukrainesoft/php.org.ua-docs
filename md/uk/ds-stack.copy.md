---
navigation:
  - ds-stack.construct.md: '« Ds\\Stack::\_\_construct'
  - ds-stack.count.md: 'Ds\\Stack::count »'
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::copy

(PECL ds >= 1.0.0)

Ds\\Stack::copy — Повертає поверхневу копію колекції

### Опис

```methodsynopsis
public Ds\Stack::copy(): Ds\Stack
```

Повертає поверхневу копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Колекція поверхнева копія.

### Приклади

**Пример #1 Пример использования**Ds\\Stack::copy()\*\*\*\*

```php
<?php
$a = new \Ds\Stack([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->push(4);

print_r($a);
print_r($b);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Stack Object
(
    [0] => 3
    [1] => 2
    [2] => 1
)
Ds\Stack Object
(
    [0] => 4
    [1] => 3
    [2] => 2
    [3] => 1
)
```
