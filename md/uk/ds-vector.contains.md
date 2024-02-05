---
navigation:
  - ds-vector.construct.md: '« Ds\\Vector::\_\_construct'
  - ds-vector.copy.md: 'Ds\\Vector::copy »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::contains'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::contains

(PECL ds >= 1.0.0)

Ds\\Vector::contains — Перевіряє, чи у векторі задані значення

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

**Пример #1 Пример использования**Ds\\Vector::contains()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
bool(false)
bool(true)
bool(true)
bool(false)
bool(true)
```
