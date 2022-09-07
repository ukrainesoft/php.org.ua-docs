---
navigation:
  - ds-vector.construct.md: '« DsVector::construct'
  - ds-vector.copy.md: 'ДсVector::copy »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::contains'
---
# ДсVector::contains

(PECL ds >= 1.0.0)

ДсVector::contains — Перевіряє, чи у векторі задані значення

### Опис

```methodsynopsis
public Ds\Vector::contains(mixed ...$values): bool
```

Перевіряє, чи у векторі задані значення.

### Список параметрів

`values`

Значення для перевірки.

### Значення, що повертаються

Повертає \*\*`false`\*\*якщо хоча б одне значення з `values` не знайдено у векторі та **`true`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсVector::contains()****

```php
<?php
$vector = new \Ds\Vector(['a', 'b', 'c', 1, 2, 3]);

var_dump($vector->contains('a'));                // true
var_dump($vector->contains('a', 'b'));           // true
var_dump($vector->contains('c', 'd'));           // false

var_dump($vector->contains(...['c', 'b', 'a'])); // true

// Всегда строгая проверка
var_dump($vector->contains(1));                  // true
var_dump($vector->contains('1'));                // false

var_dump($sequece->contains(...[]));               // true
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
bool(false)
bool(true)
bool(true)
bool(false)
bool(true)
```
