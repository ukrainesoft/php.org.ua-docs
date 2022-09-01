---
navigation:
  - class.parentiterator.md: « ParentIterator
  - parentiterator.construct.md: 'ParentIterator::construct »'
  - index.md: PHP Manual
  - class.parentiterator.md: ParentIterator
title: 'ParentIterator::accept'
---
# ParentIterator::accept

(PHP 5> = 5.1.0, PHP 7, PHP 8)

ParentIterator::accept — Визначення доступності

### Опис

```methodsynopsis
public ParentIterator::accept(): bool
```

Визначає, чи елемент має дочірні елементи.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо елемент доступний, **`false`** в іншому випадку.

### Дивіться також

-   [ParentIterator::hasChildren()](parentiterator.haschildren.md) - Перевіряє, чи має внутрішній об'єкт-ітератор дочірні об'єкти
-   [FilterIterator::accept()](filteriterator.accept.md) - Перевіряє, чи є поточний елемент ітератора допустимим
