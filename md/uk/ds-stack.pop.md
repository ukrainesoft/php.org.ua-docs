---
navigation:
  - ds-stack.peek.md: '« Ds\\Stack::peek'
  - ds-stack.push.md: 'Ds\\Stack::push »'
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::pop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::pop

(PECL ds >= 1.0.0)

Ds\\Stack::pop — Видаляє та повертає значення з вершини стека

### Опис

```methodsynopsis
public Ds\Stack::pop(): mixed
```

Видаляє та повертає значення з вершини стека.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Видалене з вершини стека значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання** Ds\\Stack::pop()\*\*\*\*

```php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c");

var_dump($stack->pop());
var_dump($stack->pop());
var_dump($stack->pop());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "c"
string(1) "b"
string(1) "a"
```
