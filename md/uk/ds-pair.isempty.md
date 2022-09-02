---
navigation:
  - ds-pair.copy.md: '« DsPair::copy'
  - ds-pair.jsonserialize.md: 'ДсPair::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-pair.md: Пара
title: 'ДсPair::isEmpty'
---
# ДсPair::isEmpty

(No version information available, might only be in Git)

ДсPair::isEmpty — Перевіряє, чи є пара порожньою

### Опис

```methodsynopsis
public Ds\Pair::isEmpty(): bool
```

Визначає, чи пара порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо пара порожня і **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсPair::isEmpty()****

```php
<?php
$a = new \Ds\Pair("a", 1);
$b = new \Ds\Pair();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```
