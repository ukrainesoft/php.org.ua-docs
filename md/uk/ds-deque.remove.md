---
navigation:
  - ds-deque.reduce.md: '« Ds\\Deque::reduce'
  - ds-deque.reverse.md: 'Ds\\Deque::reverse »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::remove

(PECL ds >= 1.0.0)

Ds\\Deque::remove — Видаляє та повертає значення за індексом

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

**Приклад #1 Приклад використання** Ds\\Deque::remove()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->remove(1));
var_dump($deque->remove(0));
var_dump($deque->remove(0));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "b"
string(1) "a"
string(1) "c"
```
