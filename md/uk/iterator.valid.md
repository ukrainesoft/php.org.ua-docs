---
navigation:
  - iterator.rewind.md: '« Iterator::rewind'
  - class.iteratoraggregate.md: IteratorAggregate »
  - index.md: PHP Manual
  - class.iterator.md: Iterator
title: 'Iterator::valid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Iterator::valid

(PHP 5, PHP 7, PHP 8)

Iterator::valid — Перевіряє коректність поточної позиції

### Опис

```methodsynopsis
public Iterator::valid(): bool
```

Метод викликається після функцій [Iterator::rewind()](iterator.rewind.md) і [Iterator::next()](iterator.next.md) щоб перевірити, чи припустима поточна позиція.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення, що повертається, буде приведено до логічного типу (bool) і потім використано. Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
