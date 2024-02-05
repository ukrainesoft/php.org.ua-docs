---
navigation:
  - ds-vector.filter.md: '« Ds\\Vector::filter'
  - ds-vector.first.md: 'Ds\\Vector::first »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::find'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::find

(PECL ds >= 1.0.0)

Ds\\Vector::find — Пошук індексу за значенням

### Опис

```methodsynopsis
public Ds\Vector::find(mixed $value): mixed
```

Повертає індекс значення `value`или\*\*`false`\*\*якщо нічого не знайдено.

### Список параметрів

`value`

Шукане значення.

### Значення, що повертаються

Індекс елемента або \*\*`false`\*\*якщо значення не знайдено.

> **Зауваження** :
> 
> Елементи порівнюються суворо (за типом та значенням).

### Приклади

**Пример #1 Пример использования**Ds\\Vector::find()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector(["a", 1, true]);

var_dump($vector->find("a")); // 0
var_dump($vector->find("b")); // false
var_dump($vector->find("1")); // false
var_dump($vector->find(1));   // 1
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(0)
bool(false)
bool(false)
int(1)
```
