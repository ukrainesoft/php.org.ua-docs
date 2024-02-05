---
navigation:
  - splheap.current.md: '« SplHeap::current'
  - splheap.insert.md: 'SplHeap::insert »'
  - index.md: PHP Manual
  - class.splheap.md: SplHeap
title: 'SplHeap::extract'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplHeap::extract

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplHeap::extract — Витягує вузол із купи та пересортує її

### Опис

```methodsynopsis
public SplHeap::extract(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення вилученого вузла.

### Помилки

Якщо структура даних вузла виявиться порожньою, буде викинуто виняток [RuntimeException](class.runtimeexception.md)
