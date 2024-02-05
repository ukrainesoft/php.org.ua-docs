---
navigation:
  - splfixedarray.offsetset.md: '« SplFixedArray::offsetSet'
  - splfixedarray.rewind.md: 'SplFixedArray::rewind »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::offsetUnset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFixedArray::offsetUnset

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplFixedArray::offsetUnset — Видаляє значення за індексом $index

### Опис

```methodsynopsis
public SplFixedArray::offsetUnset(int $index): void
```

Видаляє значення за заданим індексом.

### Список параметрів

`index`

Індекс, яким видаляється значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md), когда`index` перевищує заданий розмір масиву або коли `index` не можна розпізнати як ціле число.
