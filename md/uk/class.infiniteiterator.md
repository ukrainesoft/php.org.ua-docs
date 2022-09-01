---
navigation:
  - globiterator.count.md: '« GlobIterator::count'
  - infiniteiterator.construct.md: 'InfiniteIterator::construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас InfiniteIterator
---
# Клас InfiniteIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Клас **InfiniteIterator** дозволяє зробити нескінченний перебір ітератора без необхідності вручну перебирати ітератор до досягнення його кінця.

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

-   [InfiniteIterator::construct](infiniteiterator.construct.md) - Конструктор класу InfiniteIterator
-   [InfiniteIterator::next](infiniteiterator.next.md) — Переміщує ітератор на одну позицію вперед чи на початок
