---
navigation:
  - ds-vector.filter.html: '« DsVector::filter'
  - ds-vector.first.html: 'ДсVector::first »'
  - index.md: PHP Manual
  - class.ds-vector.html: Вектор
title: 'ДсVector::find'
---
# ДсVector::find

(PECL ds >= 1.0.0)

ДсVector::find — Пошук індексу за значенням

### Опис

```methodsynopsis
public Ds\Vector::find(mixed $value): mixed
```

Повертає індекс значення `value` або \*\*`false`\*\*якщо нічого не знайдено.

### Список параметрів

`value`

Шукане значення.

### Значення, що повертаються

Індекс елемента або \*\*`false`\*\*якщо значення не знайдено.

> **Зауваження**
> 
> Елементи порівнюються суворо (за типом та значенням).

### Приклади

**Приклад #1 Приклад використання **ДсVector::find()****

```php
<?php
$vector = new \Ds\Vector(["a", 1, true]);

var_dump($vector->find("a")); // 0
var_dump($vector->find("b")); // false
var_dump($vector->find("1")); // false
var_dump($vector->find(1));   // 1
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(0)
bool(false)
bool(false)
int(1)
```
