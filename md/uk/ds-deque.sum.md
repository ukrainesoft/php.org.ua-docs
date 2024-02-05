---
navigation:
  - ds-deque.sorted.md: '« Ds\\Deque::sorted'
  - ds-deque.toarray.md: 'Ds\\Deque::toArray »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::sum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::sum

(PECL ds >= 1.0.0)

Ds\\Deque::sum — Повертає суму всіх значень двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::sum(): int|float
```

Повертає суму всіх значень двосторонньої черги.

> **Зауваження** :
> 
> Масиви та об'єкти вважаються нулем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Сума всіх значень двосторонньої черги типів float чи int, залежно від значень двосторонньої черги.

### Приклади

**Пример #1 Пример использования**Ds\\Deque::sum()\*\* з цілими значеннями\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(6)
```

**Пример #2 Пример использования**Ds\\Deque::sum()\*\* зі значеннями типу float\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2.5, 3]);
var_dump($deque->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
float(6.5)
```
