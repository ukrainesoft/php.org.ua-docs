---
navigation:
  - ds-deque.find.md: '« Ds\\Deque::find'
  - ds-deque.get.md: 'Ds\\Deque::get »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::first'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::first

(PECL ds >= 1.0.0)

Ds\\Deque::first — Повертає перший елемент двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::first(): mixed
```

Повертає перший елемент двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент двосторонньої черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо двостороння черга порожня.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::first()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->first());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
```
