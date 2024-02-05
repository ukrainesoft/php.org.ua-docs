---
navigation:
  - ds-stack.jsonserialize.md: '« Ds\\Stack::jsonSerialize'
  - ds-stack.pop.md: 'Ds\\Stack::pop »'
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::peek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::peek

(PECL ds >= 1.0.0)

Ds\\Stack::peek — Повертає значення з вершини стека

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

**Приклад #1 Приклад використання** Ds\\Stack::peek()\*\*\*\*

```php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c");

var_dump($stack->peek());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "c"
```
