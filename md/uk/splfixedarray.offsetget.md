---
navigation:
  - splfixedarray.offsetexists.md: '« SplFixedArray::offsetExists'
  - splfixedarray.offsetset.md: 'SplFixedArray::offsetSet »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::offsetGet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFixedArray::offsetGet

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplFixedArray::offsetGet — Повертає значення за вказаним індексом

### Опис

```methodsynopsis
public SplFixedArray::offsetGet(int $index): mixed
```

Повертає значення за індексом `index`

### Список параметрів

`index`

Індекс.

### Значення, що повертаються

Значение по индексу`index`

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md), когда параметр`index` виходить за рамки заданого розміру масиву або коли `index` не можна розпізнати як ціле число.
