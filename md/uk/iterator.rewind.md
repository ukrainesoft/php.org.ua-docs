---
navigation:
  - iterator.next.md: '« Iterator::next'
  - iterator.valid.md: 'Iterator::valid »'
  - index.md: PHP Manual
  - class.iterator.md: Iterator
title: 'Iterator::rewind'
---
# Iterator::rewind

(PHP 5, PHP 7, PHP 8)

Iterator::rewind - Повертає ітератор на перший елемент

### Опис

```methodsynopsis
public Iterator::rewind(): void
```

Повертає ітератор назад перший елемент.

> **Зауваження**
> 
> На початку циклу [foreach](control-structures.foreach.md) цей метод викликається *першим*. Метод *не буде* викликаний *після* циклу [foreach](control-structures.foreach.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Будь-яке значення, що повертається, ігнорується.
