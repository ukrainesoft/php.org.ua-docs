---
navigation:
  - spldoublylinkedlist.offsetget.md: '« SplDoublyLinkedList::offsetGet'
  - spldoublylinkedlist.offsetunset.md: 'SplDoublyLinkedList::offsetUnset »'
  - index.md: PHP Manual
  - class.spldoublylinkedlist.md: SplDoublyLinkedList
title: 'SplDoublyLinkedList::offsetSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplDoublyLinkedList::offsetSet

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplDoublyLinkedList::offsetSet — Встановлює значення за заданим індексом $index у $value

### Опис

```methodsynopsis
public SplDoublyLinkedList::offsetSet(?int $index, mixed $value): void
```

Устанавливает значение по заданному индексу`index`в`value`

### Список параметрів

`index`

Індекс. Якщо **`null`**, наступне значення буде додано після останнього елемента.

`value`

Новое значение для индекса`index`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md), когда`index` виходить за межі, або коли `index` може бути представлений як цілого числа.
