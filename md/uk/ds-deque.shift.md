---
navigation:
  - ds-deque.set.md: '« Ds\\Deque::set'
  - ds-deque.slice.md: 'Ds\\Deque::slice »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::shift'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::shift

(PECL ds >= 1.0.0)

Ds\\Deque::shift — Видаляє та повертає перше значення

### Опис

```methodsynopsis
public Ds\Deque::shift(): mixed
```

Видаляє та повертає перше значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перше віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо двостороння черга порожня.

### Приклади

**Пример #1 Пример использования**Ds\\Deque::shift()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->shift());
var_dump($deque->shift());
var_dump($deque->shift());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
