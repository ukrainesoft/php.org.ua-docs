---
navigation:
  - splheap.current.html: '« SplHeap::current'
  - splheap.insert.html: 'SplHeap::insert »'
  - index.html: PHP Manual
  - class.splheap.html: SplHeap
title: 'SplHeap::extract'
---
# SplHeap::extract

(PHP 5> = 5.3.0, PHP 7, PHP 8)

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
