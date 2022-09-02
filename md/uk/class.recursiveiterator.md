---
navigation:
  - outeriterator.getinneriterator.md: '« OuterIterator::getInnerIterator'
  - recursiveiterator.getchildren.md: 'RecursiveIterator::getChildren »'
  - index.md: PHP Manual
  - spl.interfaces.md: Інтерфейси
title: Інтерфейс RecursiveIterator
---
# Інтерфейс RecursiveIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Класи, що реалізують **RecursiveIterator**можуть бути використані для рекурсивного перебору ітераторів.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface RecursiveIterator
      extends
       Iterator
     
     {

    /* Методы */
    
   public getChildren(): ?RecursiveIterator
public hasChildren(): bool


    /* Наследуемые методы */
    public Iterator::current(): mixed
public Iterator::key(): mixed
public Iterator::next(): void
public Iterator::rewind(): void
public Iterator::valid(): bool

   }
```

## Зміст

-   [RecursiveIterator::getChildren](recursiveiterator.getchildren.md) — Повертає ітератор до поточного елемента
-   [RecursiveIterator::hasChildren](recursiveiterator.haschildren.md) — Визначає, чи можна створити ітератор для поточного елемента.
