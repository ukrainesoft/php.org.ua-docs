---
navigation:
  - ds-vector.sum.md: '« DsVector::sum'
  - ds-vector.unshift.md: 'ДсVector::unshift »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::toArray'
---
# ДсVector::toArray

(PECL ds >= 1.0.0)

ДсVector::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Vector::toArray(): array
```

Перетворює колекцію на масив (array).

> **Зауваження**
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array), що містить всі елементи колекції зі збереженням їхнього порядку.

### Приклади

**Приклад #1 Приклад використання **ДсVector::toArray()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->toArray());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
