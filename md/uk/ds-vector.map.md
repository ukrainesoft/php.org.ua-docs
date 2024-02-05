---
navigation:
  - ds-vector.last.md: '« Ds\\Vector::last'
  - ds-vector.merge.md: 'Ds\\Vector::merge »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::map'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::map

(PECL ds >= 1.0.0)

Ds\\Vector::map — Повертає результат застосування callback-функції до всіх значень вектора

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

Аргумент типа[callable](language.types.callable.md)

Ця функція має повертати нове значення для кожного елемента вектора.

### Значення, що повертаються

Результат применения`callback` до кожного значення вектора.

> **Зауваження** :
> 
> Значення поточної колекції залишаться незмінними.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::map()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

print_r($vector->map(function($value) { return $value * 2; }));
print_r($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

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
