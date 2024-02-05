---
navigation:
  - ds-stack.push.md: '« Ds\\Stack::push'
  - class.ds-queue.md: Ds\\Queue »
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::toArray

(PECL ds >= 1.0.0)

Ds\\Stack::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Stack::toArray(): array
```

Перетворює колекцію на array.

> **Зауваження** :
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить всі елементи колекції зі збереженням їхнього порядку.

### Приклади

**Приклад #1 Приклад использования метода**Ds\\Stack::toArray()\*\*\*\*

```php
<?php
$stack = new \Ds\Stack([1, 2, 3]);

var_dump($stack->toArray());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  [0]=>
  int(3)
  [1]=>
  int(2)
  [2]=>
  int(1)
}
```
