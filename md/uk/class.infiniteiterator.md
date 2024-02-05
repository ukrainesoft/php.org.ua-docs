---
navigation:
  - globiterator.count.md: '« GlobIterator::count'
  - infiniteiterator.construct.md: 'InfiniteIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас InfiniteIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас InfiniteIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Класс**InfiniteIterator** дозволяє зробити нескінченний перебір ітератора без необхідності вручну перебирати ітератор до досягнення його кінця.

## Огляд класів

```classsynopsis

    
     class InfiniteIterator
    

    
     extends
      IteratorIterator
     {

    /* Методы */
    
   public __construct(Iterator $iterator)

    public next(): void


    /* Наследуемые методы */
    public IteratorIterator::current(): mixed
public IteratorIterator::getInnerIterator(): ?Iterator
public IteratorIterator::key(): mixed
public IteratorIterator::next(): void
public IteratorIterator::rewind(): void
public IteratorIterator::valid(): bool

   }
```

## Зміст

-   [InfiniteIterator::\_\_construct](infiniteiterator.construct.md) \- Конструктор класу InfiniteIterator
-   [InfiniteIterator::next](infiniteiterator.next.md)— Переміщує ітератор на одну позицію вперед чи на початок
