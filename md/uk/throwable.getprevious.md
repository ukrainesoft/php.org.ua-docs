---
navigation:
  - throwable.gettraceasstring.md: '« Throwable::getTraceAsString'
  - throwable.tostring.md: 'Throwable::\_\_toString »'
  - index.md: PHP Manual
  - class.throwable.md: Throwable
title: 'Throwable::getPrevious'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Throwable::getPrevious

(PHP 7, PHP 8)

Throwable::getPrevious — Повертає попередній Throwable

### Опис

```methodsynopsis
public Throwable::getPrevious(): ?Throwable
```

Повертає будь-який попередній Throwable (для прикладу, передане третім параметром [Exception::\_\_construct()](exception.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній [Throwable](class.throwable.md), если он доступен, или\*\*`null`\*\* в іншому випадку.

### Дивіться також

-   [Exception::getPrevious()](exception.getprevious.md) \- Повертає попередній об'єкт, що реалізує Throwable
