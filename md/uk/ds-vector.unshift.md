---
navigation:
  - ds-vector.toarray.md: '« Ds\\Vector::toArray'
  - class.ds-deque.md: Ds\\Deque »
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::unshift'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::unshift

(PECL ds >= 1.0.0)

Ds\\Vector::unshift — Додає значення на початок вектора

### Опис

```methodsynopsis
public Ds\Vector::unshift(mixed $values = ?): void
```

Додає значення початку вектора, зрушуючи всі елементи вперед, щоб звільнити місце для нових.

### Список параметрів

`values`

Значення, що додаються.

> **Зауваження** :
> 
> Багато значень додаються в тому порядку, як вони були передані.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::unshift()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

$vector->unshift("a");
$vector->unshift("b", "c");

print_r($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

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
