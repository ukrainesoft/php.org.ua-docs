---
navigation:
  - ds-stack.push.md: '« DsStack::push'
  - class.ds-queue.md: Черга »
  - index.md: PHP Manual
  - class.ds-stack.md: Стек
title: 'ДсStack::toArray'
---
# ДсStack::toArray

(PECL ds >= 1.0.0)

ДсStack::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Stack::toArray(): array
```

Перетворює колекцію на array.

> **Зауваження**
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array), що містить всі елементи колекції із збереженням їхнього порядку.

### Приклади

**Приклад #1 Приклад використання **ДсStack::toArray()****

```php
<?php
$stack = new \Ds\Stack([1, 2, 3]);

var_dump($stack->toArray());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
