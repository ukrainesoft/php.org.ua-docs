---
navigation:
  - ds-stack.peek.md: '« DsStack::peek'
  - ds-stack.push.md: 'ДсStack::push »'
  - index.md: PHP Manual
  - class.ds-stack.md: Стек
title: 'ДсStack::pop'
---
# ДсStack::pop

(PECL ds >= 1.0.0)

ДсStack::pop — Видаляє та повертає значення з вершини стека

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

**Приклад #1 Приклад використання **ДсStack::pop()****

```php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c");

var_dump($stack->pop());
var_dump($stack->pop());
var_dump($stack->pop());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "c"
string(1) "b"
string(1) "a"
```
