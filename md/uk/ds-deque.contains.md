---
navigation:
  - ds-deque.construct.html: '« DsDeque::construct'
  - ds-deque.copy.html: 'ДсDeque::copy »'
  - index.md: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::contains'
---
# ДсDeque::contains

(PECL ds >= 1.0.0)

ДсDeque::contains — Перевіряє, чи є у двосторонній черзі задані значення

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

**Приклад #1 Приклад використання **ДсDeque::contains()****

```php
<?php
$deque = new \Ds\Deque(['a', 'b', 'c', 1, 2, 3]);

var_dump($deque->contains('a'));                // true
var_dump($deque->contains('a', 'b'));           // true
var_dump($deque->contains('c', 'd'));           // false

var_dump($deque->contains(...['c', 'b', 'a'])); // true

// Всегда строгая проверка
var_dump($deque->contains(1));                  // true
var_dump($deque->contains('1'));                // false

var_dump($sequece->contains(...[]));               // true
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
