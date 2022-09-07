---
navigation:
  - ds-deque.filter.md: '« DsDeque::filter'
  - ds-deque.first.md: 'ДсDeque::first »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::find'
---
# ДсDeque::find

(PECL ds >= 1.0.0)

ДсDeque::find — Пошук індексу за значенням

### Опис

```methodsynopsis
public Ds\Deque::find(mixed $value): mixed
```

Повертає індекс значення `value` або \*\*`false`\*\*якщо нічого не знайдено.

### Список параметрів

`value`

Шукане значення.

### Значення, що повертаються

Індекс елемента або \*\*`false`\*\*якщо значення не знайдено.

> **Зауваження**
> 
> Елементи порівнюються суворо (за типом та значенням).

### Приклади

**Приклад #1 Приклад використання **ДсDeque::find()****

```php
<?php
$deque = new \Ds\Deque(["a", 1, true]);

var_dump($deque->find("a")); // 0
var_dump($deque->find("b")); // false
var_dump($deque->find("1")); // false
var_dump($deque->find(1));   // 1
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(0)
bool(false)
bool(false)
int(1)
```
