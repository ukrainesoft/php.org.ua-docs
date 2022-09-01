---
navigation:
  - throwable.gettraceasstring.html: '« Throwable::getTraceAsString'
  - throwable.tostring.html: 'Throwable::toString »'
  - index.html: PHP Manual
  - class.throwable.html: Throwable
title: 'Throwable::getPrevious'
---
# Throwable::getPrevious

(PHP 7, PHP 8)

Throwable::getPrevious — Повертає попередній Throwable

### Опис

```methodsynopsis
public Throwable::getPrevious(): ?Throwable
```

Повертає будь-який попередній Throwable (для прикладу, передане третім параметром [Exception::construct()](exception.construct.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній [Throwable](class.throwable.html), якщо він доступний, або **`null`** в іншому випадку.

### Дивіться також

-   [Exception::getPrevious()](exception.getprevious.html) - Повертає попередній об'єкт, що реалізує Throwable
