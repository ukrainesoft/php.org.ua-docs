---
navigation:
  - ds-stack.count.md: '« Ds\\Stack::count'
  - ds-stack.jsonserialize.md: 'Ds\\Stack::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::isEmpty

(PECL ds >= 1.0.0)

Ds\\Stack::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\Stack::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если коллекция пуста, и\*\*`false`\*\* в іншому випадку.

### Приклади

**Пример #1 Пример использования**Ds\\Stack::isEmpty()\*\*\*\*

```php
<?php
$a = new \Ds\Stack([1, 2, 3]);
$b = new \Ds\Stack();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```
