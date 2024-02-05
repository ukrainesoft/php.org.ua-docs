---
navigation:
  - ds-deque.rotate.md: '« Ds\\Deque::rotate'
  - ds-deque.shift.md: 'Ds\\Deque::shift »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::set

(PECL ds >= 1.0.0)

Ds\\Deque::set — Замінює значення за вказаним індексом

### Опис

```methodsynopsis
public Ds\Deque::set(int $index, mixed $value): void
```

Замінює значення за вказаним індексом.

### Список параметрів

`index`

Індекс, яким треба замінити значення.

`value`

Нове значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::set()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

$deque->set(1, "_");
print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => a
    [1] => _
    [2] => c
)
```

**Приклад #2 Приклад використання** Ds\\Deque::set()\*\* із синтаксисом масиву\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

$deque[1] = "_";
print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => a
    [1] => _
    [2] => c
)
```
