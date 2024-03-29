---
navigation:
  - class.spldoublylinkedlist.md: « SplDoublyLinkedList
  - spldoublylinkedlist.bottom.md: 'SplDoublyLinkedList::bottom »'
  - index.md: PHP Manual
  - class.spldoublylinkedlist.md: SplDoublyLinkedList
title: 'SplDoublyLinkedList::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplDoublyLinkedList::add

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

SplDoublyLinkedList::add — Додає/вставляє нове значення за вказаним індексом

### Опис

```methodsynopsis
public SplDoublyLinkedList::add(int $index, mixed $value): void
```

Вставляет значение`value`по указанному индексу`index`. Попереднє значення (і всі наступні) зміщуються вгору за списком.

### Список параметрів

`index`

Індекс, яким треба вставити значення.

`value`

Значення, яке потрібно вставити за індексом `index`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md), якщо `index` за межами списку, або якщо `index` може бути представлений як цілого числа.
