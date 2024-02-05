---
navigation:
  - ds-deque.filter.md: '« Ds\\Deque::filter'
  - ds-deque.first.md: 'Ds\\Deque::first »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::find'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::find

(PECL ds >= 1.0.0)

Ds\\Deque::find — Пошук індексу за значенням

### Опис

```methodsynopsis
public Ds\Deque::find(mixed $value): mixed
```

Повертає індекс значення `value`или\*\*`false`\*\*якщо нічого не знайдено.

### Список параметрів

`value`

Шукане значення.

### Значення, що повертаються

Індекс елемента або \*\*`false`\*\*якщо значення не знайдено.

> **Зауваження** :
> 
> Елементи порівнюються суворо (за типом та значенням).

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::find()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", 1, true]);

var_dump($deque->find("a")); // 0
var_dump($deque->find("b")); // false
var_dump($deque->find("1")); // false
var_dump($deque->find(1));   // 1
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(0)
bool(false)
bool(false)
int(1)
```
