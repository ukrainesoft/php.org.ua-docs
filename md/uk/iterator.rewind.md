---
navigation:
  - iterator.next.html: '« Iterator::next'
  - iterator.valid.html: 'Iterator::valid »'
  - index.html: PHP Manual
  - class.iterator.html: Iterator
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
> На початку циклу [foreach](control-structures.foreach.html) цей метод викликається *першим*. Метод *не буде* викликаний *після* циклу [foreach](control-structures.foreach.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Будь-яке значення, що повертається, ігнорується.
