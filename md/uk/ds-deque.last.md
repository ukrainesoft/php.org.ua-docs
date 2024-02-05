---
navigation:
  - ds-deque.jsonserialize.md: '« Ds\\Deque::jsonSerialize'
  - ds-deque.map.md: 'Ds\\Deque::map »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::last'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::last

(PECL ds >= 1.0.0)

Ds\\Deque::last — Повертає останнє значення двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::last(): mixed
```

Повертає останнє значення двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент двосторонньої черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md), якщо двостороння черга порожня.

### Приклади

**Пример #1 Пример использования**Ds\\Deque::last()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->last());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
```
