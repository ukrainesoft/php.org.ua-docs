---
navigation:
  - outeriterator.getinneriterator.html: '« OuterIterator::getInnerIterator'
  - recursiveiterator.getchildren.html: 'RecursiveIterator::getChildren »'
  - index.html: PHP Manual
  - spl.interfaces.html: Інтерфейси
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

-   [RecursiveIterator::getChildren](recursiveiterator.getchildren.html) — Повертає ітератор до поточного елемента
-   [RecursiveIterator::hasChildren](recursiveiterator.haschildren.html) — Визначає, чи можна створити ітератор для поточного елемента.
