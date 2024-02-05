---
navigation:
  - splheap.valid.md: '« SplHeap::valid'
  - splmaxheap.compare.md: 'SplMaxHeap::compare »'
  - index.md: PHP Manual
  - spl.datastructures.md: Структури даних
title: Клас SplMaxHeap
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SplMaxHeap

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplMaxHeap надає основні функціональні можливості купи, зберігаючи максимальний елемент нагорі.

## Огляд класів

```classsynopsis

    
     class SplMaxHeap
    

    
     extends
      SplHeap
     {

    /* Методы */
    
   protected compare(mixed $value1, mixed $value2): int


    /* Наследуемые методы */
    protected SplHeap::compare(mixed $value1, mixed $value2): int
public SplHeap::count(): int
public SplHeap::current(): mixed
public SplHeap::extract(): mixed
public SplHeap::insert(mixed $value): true
public SplHeap::isCorrupted(): bool
public SplHeap::isEmpty(): bool
public SplHeap::key(): int
public SplHeap::next(): void
public SplHeap::recoverFromCorruption(): bool
public SplHeap::rewind(): void
public SplHeap::top(): mixed
public SplHeap::valid(): bool

   }
```

## Зміст

-   [SplMaxHeap::compare](splmaxheap.compare.md)— Порівнює елементи, щоб під час сортування коректно розмістити їх у купі
