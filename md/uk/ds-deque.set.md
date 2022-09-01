---
navigation:
  - ds-deque.rotate.html: '« DsDeque::rotate'
  - ds-deque.shift.html: 'ДсDeque::shift »'
  - index.md: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::set'
---
# ДсDeque::set

(PECL ds >= 1.0.0)

ДсDeque::set — Замінює значення за вказаним індексом

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

**Приклад #1 Приклад використання **ДсDeque::set()****

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

$deque->set(1, "_");
print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Deque Object
(
    [0] => a
    [1] => _
    [2] => c
)
```

**Приклад #2 Приклад використання **ДсDeque::set()** із синтаксисом масиву**

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

$deque[1] = "_";
print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Deque Object
(
    [0] => a
    [1] => _
    [2] => c
)
```
