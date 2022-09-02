---
navigation:
  - ds-deque.reduce.md: '« DsDeque::reduce'
  - ds-deque.reverse.md: 'ДсDeque::reverse »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::remove'
---
# ДсDeque::remove

(PECL ds >= 1.0.0)

ДсDeque::remove — Видаляє та повертає значення за індексом

### Опис

```methodsynopsis
public Ds\Deque::remove(int $index): mixed
```

Видаляє та повертає значення за індексом.

### Список параметрів

`index`

Індекс, яким необхідно видалити значення.

### Значення, що повертаються

Віддалене значення.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::remove()****

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->remove(1));
var_dump($deque->remove(0));
var_dump($deque->remove(0));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "b"
string(1) "a"
string(1) "c"
```
