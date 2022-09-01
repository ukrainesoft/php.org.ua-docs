---
navigation:
  - yac.getter.md: '« Yac::get'
  - yac.set.md: 'Yac::set »'
  - index.md: PHP Manual
  - class.yac.md: Yac
title: 'Yac::info'
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

Повернути відповідний масив: "memorysize", "slotsmemorysize", "valuesmemorysize", "segmentsize", "segmentnum", "miss", "hits", "fails", "kicks", "recycles", "slotssize", "slotsused"
