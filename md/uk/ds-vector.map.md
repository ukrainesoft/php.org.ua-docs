---
navigation:
  - ds-vector.last.html: '« DsVector::last'
  - ds-vector.merge.html: 'ДсVector::merge »'
  - index.md: PHP Manual
  - class.ds-vector.html: Вектор
title: 'ДсVector::map'
---
# ДсVector::map

(PECL ds >= 1.0.0)

ДсVector::map — Повертає результат застосування callback-функції до всіх значень вектора

### Опис

```methodsynopsis
public Ds\Vector::map(callable $callback): Ds\Vector
```

Повертає результат застосування callback-функції, переданої в `callback`до всіх значень вектора.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Аргумент типу [callable](language.types.callable.md)

Ця функція має повертати нове значення для кожного елемента вектора.

### Значення, що повертаються

Результат застосування `callback` до кожного значення вектора.

> **Зауваження**
> 
> Значення поточної колекції залишаться незмінними.

### Приклади

**Приклад #1 Приклад використання **ДсVector::map()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

print_r($vector->map(function($value) { return $value * 2; }));
print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
```
