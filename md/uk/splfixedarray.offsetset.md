---
navigation:
  - splfixedarray.offsetget.md: '« SplFixedArray::offsetGet'
  - splfixedarray.offsetunset.md: 'SplFixedArray::offsetUnset »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::offsetSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFixedArray::offsetSet

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplFixedArray::offsetSet — Встановлює нове значення за заданим індексом

### Опис

```methodsynopsis
public SplFixedArray::offsetSet(int $index, mixed $value): void
```

По индексу`index`устанавливает значение`value`

### Список параметрів

`index`

Індекс, яким встановлюється значення.

`value`

Новое значение для индекса`index`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md), когда`index` перевищує заданий розмір масиву або коли `index` не можна розпізнати як ціле число.
