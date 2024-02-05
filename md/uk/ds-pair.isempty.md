---
navigation:
  - ds-pair.copy.md: '« Ds\\Pair::copy'
  - ds-pair.jsonserialize.md: 'Ds\\Pair::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-pair.md: Ds\\Pair
title: 'Ds\\Pair::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Pair::isEmpty

(No version information available, might only be in Git)

Ds\\Pair::isEmpty — Перевіряє, чи є пара порожньою

### Опис

```methodsynopsis
public Ds\Pair::isEmpty(): bool
```

Визначає, чи пара порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если пара пустая и\*\*`false`\*\* в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** Ds\\Pair::isEmpty()\*\*\*\*

```php
<?php
$a = new \Ds\Pair("a", 1);
$b = new \Ds\Pair();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```
