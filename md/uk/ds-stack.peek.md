---
navigation:
  - ds-stack.jsonserialize.md: '« DsStack::jsonSerialize'
  - ds-stack.pop.md: 'ДсStack::pop »'
  - index.md: PHP Manual
  - class.ds-stack.md: Стек
title: 'ДсStack::peek'
---
# ДсStack::peek

(PECL ds >= 1.0.0)

ДсStack::peek — Повертає значення з вершини стека

### Опис

```methodsynopsis
public Ds\Stack::peek(): mixed
```

Повертає значення з вершини стека, але не видаляє його.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення з вершини стека.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсStack::peek()****

```php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c");

var_dump($stack->peek());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "c"
```
