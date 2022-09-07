---
navigation:
  - throwable.gettraceasstring.md: '« Throwable::getTraceAsString'
  - throwable.tostring.md: 'Throwable::toString »'
  - index.md: PHP Manual
  - class.throwable.md: Throwable
title: 'Throwable::getPrevious'
---
# Throwable::getPrevious

(PHP 7, PHP 8)

Throwable::getPrevious — Повертає попередній Throwable

### Опис

```methodsynopsis
public Throwable::getPrevious(): ?Throwable
```

Повертає будь-який попередній Throwable (для прикладу, передане третім параметром [Exception::construct()](exception.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній [Throwable](class.throwable.md), якщо він доступний, або **`null`** в іншому випадку.

### Дивіться також

-   [Exception::getPrevious()](exception.getprevious.md) - Повертає попередній об'єкт, що реалізує Throwable
