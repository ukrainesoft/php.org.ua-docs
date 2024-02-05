---
navigation:
  - ds-deque.toarray.md: '« Ds\\Deque::toArray'
  - class.ds-map.md: Ds\\Map »
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::unshift'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::unshift

(PECL ds >= 1.0.0)

Ds\\Deque::unshift — Додає значення на початок двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::unshift(mixed $values = ?): void
```

Додає значення початку двосторонньої черги, зрушуючи всі елементи вперед, щоб звільнити місце для нових.

### Список параметрів

`values`

Значення, що додаються.

> **Зауваження** :
> 
> Багато значень додаються в тому порядку, як вони були передані.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Deque::unshift()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

$deque->unshift("a");
$deque->unshift("b", "c");

print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

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
