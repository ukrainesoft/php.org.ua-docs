---
navigation:
  - weakmap.offsetexists.md: '« WeakMap::offsetExists'
  - weakmap.offsetset.md: 'WeakMap::offsetSet »'
  - index.md: PHP Manual
  - class.weakmap.md: WeakMap
title: 'WeakMap::offsetGet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# WeakMap::offsetGet

(PHP 8)

WeakMap::offsetGet — Повертає значення, на яке вказує певний об'єкт

### Опис

```methodsynopsis
public WeakMap::offsetGet(object $object): mixed
```

Повертає значення, яке вказує певний об'єкт.

### Список параметрів

`object`

Якийсь об'єкт міститься як ключ у колекції (map).

### Значення, що повертаються

Повертає значення, пов'язане з об'єктом, переданим як аргумент або **`null`** в іншому випадку.
