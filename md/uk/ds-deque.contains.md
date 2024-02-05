---
navigation:
  - ds-deque.construct.md: '« Ds\\Deque::\_\_construct'
  - ds-deque.copy.md: 'Ds\\Deque::copy »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::contains'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::contains

(PECL ds >= 1.0.0)

Ds\\Deque::contains — Перевіряє, чи є у двосторонній черзі задані значення

### Опис

```methodsynopsis
public Ds\Deque::contains(mixed ...$values): bool
```

Перевіряє, чи міститься у двосторонній черзі задані значення.

### Список параметрів

`values`

Значення для перевірки.

### Значення, що повертаються

Повертає \*\*`false`\*\*якщо хоча б одне значення з `values` не знайдено в колекції та **`true`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::contains()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(['a', 'b', 'c', 1, 2, 3]);

var_dump($deque->contains('a'));                // true
var_dump($deque->contains('a', 'b'));           // true
var_dump($deque->contains('c', 'd'));           // false

var_dump($deque->contains(...['c', 'b', 'a'])); // true

// Всегда строгая проверка
var_dump($deque->contains(1));                  // true
var_dump($deque->contains('1'));                // false

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
