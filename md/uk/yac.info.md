---
navigation:
  - yac.getter.md: '« Yac::\_\_get'
  - yac.set.md: 'Yac::set »'
  - index.md: PHP Manual
  - class.yac.md: Yac
title: 'Yac::info'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yac::info

(PECL yac >= 1.0.0)

Yac::info — Стан кешу

### Опис

```methodsynopsis
public Yac::info(): array
```

Отримує статус кеш-системи

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повернути відповідний масив: "memory\_size", "slots\_memory\_size", "values\_memory\_size", "segment\_size", "segment\_num", "miss", "hits", "fails", "kicks", "recycles", "slots\_size", "slots\_used"
