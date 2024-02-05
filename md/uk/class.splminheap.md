---
navigation:
  - splmaxheap.compare.md: '« SplMaxHeap::compare'
  - splminheap.compare.md: 'SplMinHeap::compare »'
  - index.md: PHP Manual
  - spl.datastructures.md: Структури даних
title: Клас SplMinHeap
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SplMinHeap

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplMinHeap надає основні функціональні можливості купи, зберігаючи мінімальний елемент нагорі.

## Огляд класів

```classsynopsis

    
     class SplMinHeap
    

    
     extends
      SplHeap
     {

    /* Методы */
    
   protectedcompare(mixed $value1, mixed $value2): int


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

-   [SplMinHeap::compare](splminheap.compare.md)— Порівнює елементи, щоб під час сортування коректно розмістити їх у купі
