---
navigation:
  - weakmap.offsetget.md: '« WeakMap::offsetGet'
  - weakmap.offsetunset.md: 'WeakMap::offsetUnset »'
  - index.md: PHP Manual
  - class.weakmap.md: WeakMap
title: 'WeakMap::offsetSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# WeakMap::offsetSet

(PHP 8)

WeakMap::offsetSet — Оновлює колекцію (map) новою парою ключ-значення

### Опис

```methodsynopsis
public WeakMap::offsetSet(object $object, mixed $value): void
```

Оновлює колекцію (map) новою парою ключ-значення. Якщо ключ уже існує в колекції, старе значення замінюється на новий.

### Список параметрів

`object`

Об'єкт, що є ключем пари ключ-значення.

`value`

Довільні дані, що служать значенням пари ключ-значення.

### Значення, що повертаються

Функція не повертає значення після виконання.
