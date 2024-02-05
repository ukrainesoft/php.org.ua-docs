---
navigation:
  - countable.count.md: '« Countable::count'
  - outeriterator.getinneriterator.md: 'OuterIterator::getInnerIterator »'
  - index.md: PHP Manual
  - spl.interfaces.md: Інтерфейси
title: Інтерфейс OuterIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс OuterIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Класи, що реалізують **OuterIterator**, можуть бути використані для перебору ітераторів

## Огляд інтерфейсів

```classsynopsis

    
     interface OuterIterator

    extends
      Iterator {

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

-   [OuterIterator::getInnerIterator](outeriterator.getinneriterator.md)— Повертає внутрішній ітератор для поточного елемента
