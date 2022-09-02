---
navigation:
  - ds-deque.toarray.md: '« DsDeque::toArray'
  - class.ds-map.md: Коллекция пар ключ-значение »
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::unshift'
---
# ДсDeque::unshift

(PECL ds >= 1.0.0)

ДсDeque::unshift — Додає значення на початок двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::unshift(mixed $values = ?): void
```

Додає значення початку двосторонньої черги, зрушуючи всі елементи вперед, щоб звільнити місце для нових.

### Список параметрів

`values`

Значення, що додаються.

> **Зауваження**
> 
> Багато значень додаються в тому порядку, як вони були передані.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::unshift()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

$deque->unshift("a");
$deque->unshift("b", "c");

print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Deque Object
(
    [0] => b
    [1] => c
    [2] => a
    [3] => 1
    [4] => 2
    [5] => 3
)
```
