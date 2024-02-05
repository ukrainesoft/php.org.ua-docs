---
navigation:
  - weakmap.getiterator.md: '« WeakMap::getIterator'
  - weakmap.offsetget.md: 'WeakMap::offsetGet »'
  - index.md: PHP Manual
  - class.weakmap.md: WeakMap
title: 'WeakMap::offsetExists'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# WeakMap::offsetExists

(PHP 8)

WeakMap::offsetExists — Перевіряє, чи є у колекції (map) певний об'єкт

### Опис

```methodsynopsis
public WeakMap::offsetExists(object $object): bool
```

Перевіряє, чи є посилання на переданий об'єкт у колекції (map).

### Список параметрів

`object`

Об'єкт перевірки.

### Значення, що повертаються

Повертає **`true`**, якщо об'єкт міститься в колекції (map) або **`false`** в іншому випадку.
