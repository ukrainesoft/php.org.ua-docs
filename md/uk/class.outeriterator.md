Інтерфейс OuterIterator

-   [« Countable::count](countable.count.html)
    
-   [OuterIterator::getInnerIterator »](outeriterator.getinneriterator.html)
    
-   [PHP Manual](index.html)
    
-   [Интерфейсы](spl.interfaces.html)
    
-   Інтерфейс OuterIterator
    

# Інтерфейс OuterIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Класи, що реалізують **OuterIterator**, можуть бути використані для перебору ітераторів

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface OuterIterator
      extends
       Iterator
     
     {

    /* Методы */
    
   public getInnerIterator(): ?Iterator


    /* Наследуемые методы */
    public Iterator::current(): mixed
public Iterator::key(): mixed
public Iterator::next(): void
public Iterator::rewind(): void
public Iterator::valid(): bool

   }
```

## Зміст

-   [OuterIterator::getInnerIterator](outeriterator.getinneriterator.html) — Повертає внутрішній ітератор для поточного елемента