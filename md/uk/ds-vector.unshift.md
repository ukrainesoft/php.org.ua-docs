---
navigation:
  - ds-vector.toarray.md: '« DsVector::toArray'
  - class.ds-deque.md: Двостороння черга »
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::unshift'
---
# ДсVector::unshift

(PECL ds >= 1.0.0)

ДсVector::unshift — Додає значення на початок вектора

### Опис

```methodsynopsis
public Ds\Vector::unshift(mixed $values = ?): void
```

Додає значення початку вектора, зрушуючи всі елементи вперед, щоб звільнити місце для нових.

### Список параметрів

`values`

Значення, що додаються.

> **Зауваження**
> 
> Багато значень додаються в тому порядку, як вони були передані.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::unshift()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

$vector->unshift("a");
$vector->unshift("b", "c");

print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => b
    [1] => c
    [2] => a
    [3] => 1
    [4] => 2
    [5] => 3
)
```
