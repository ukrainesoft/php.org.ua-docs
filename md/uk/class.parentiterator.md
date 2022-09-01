---
navigation:
  - norewinditerator.valid.html: '« NoRewindIterator::valid'
  - parentiterator.accept.html: 'ParentIterator::accept »'
  - index.html: PHP Manual
  - spl.iterators.html: Ітератори
title: Клас ParentIterator
---
# Клас ParentIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Це розширений клас від [FilterIterator](class.filteriterator.html), що дозволяє здійснити рекурсивну ітерацію, використовуючи клас [RecursiveIteratorIterator](class.recursiveiteratoriterator.html)що показує тільки ті елементи, які мають нащадків.

## Огляд класів

```classsynopsis

     
    

    
     
      class ParentIterator
     

     
      extends
       RecursiveFilterIterator
     
     {

    /* Методы */
    
   public __construct(RecursiveIterator $iterator)

    public accept(): bool
public getChildren(): ParentIterator
public hasChildren(): bool
public next(): void
public rewind(): void


    /* Наследуемые методы */
    public RecursiveFilterIterator::getChildren(): ?RecursiveFilterIterator
public RecursiveFilterIterator::hasChildren(): bool

    public FilterIterator::accept(): bool
public FilterIterator::current(): mixed
public FilterIterator::getInnerIterator(): Iterator
public FilterIterator::key(): mixed
public FilterIterator::next(): void
public FilterIterator::rewind(): void
public FilterIterator::valid(): bool

    public IteratorIterator::current(): mixed
public IteratorIterator::getInnerIterator(): ?Iterator
public IteratorIterator::key(): mixed
public IteratorIterator::next(): void
public IteratorIterator::rewind(): void
public IteratorIterator::valid(): bool

   }
```

## Зміст

-   [ParentIterator::accept](parentiterator.accept.html) — Визначення доступності
-   [ParentIterator::construct](parentiterator.construct.html) - Конструктор класу ParentIterator
-   [ParentIterator::getChildren](parentiterator.getchildren.html) — Повертає дочірні об'єкти ітератора, що зберігається всередині ParentIterator
-   [ParentIterator::hasChildren](parentiterator.haschildren.html) — Перевіряє, чи має внутрішній об'єкт-ітератор дочірні об'єкти
-   [ParentIterator::next](parentiterator.next.html) — Переміщує вказівник на одну позицію вперед
-   [ParentIterator::rewind](parentiterator.rewind.html) - Перекладає ітератор на початок
