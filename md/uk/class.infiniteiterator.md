Клас InfiniteIterator

-   [« GlobIterator::count](globiterator.count.html)
    
-   [InfiniteIterator::\_\_construct »](infiniteiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Итераторы](spl.iterators.html)
    
-   Клас InfiniteIterator
    

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

-   [InfiniteIterator::\_\_construct](infiniteiterator.construct.html) - Конструктор класу InfiniteIterator
-   [InfiniteIterator::next](infiniteiterator.next.html) — Переміщує ітератор на одну позицію вперед чи на початок