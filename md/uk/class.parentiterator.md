---
navigation:
  - norewinditerator.valid.md: '« NoRewindIterator::valid'
  - parentiterator.accept.md: 'ParentIterator::accept »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас ParentIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ParentIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Це розширений клас від [FilterIterator](class.filteriterator.md), позволяющий осуществить рекурсивную итерацию, используя класс[RecursiveIteratorIterator](class.recursiveiteratoriterator.md)що показує тільки ті елементи, які мають нащадків.

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

-   [ParentIterator::accept](parentiterator.accept.md)— Визначення доступності
-   [ParentIterator::\_\_construct](parentiterator.construct.md) \- Конструктор класу ParentIterator
-   [ParentIterator::getChildren](parentiterator.getchildren.md)— Повертає дочірні об'єкти ітератора, що зберігається всередині ParentIterator
-   [ParentIterator::hasChildren](parentiterator.haschildren.md)— Перевіряє, чи має внутрішній об'єкт-ітератор дочірні об'єкти
-   [ParentIterator::next](parentiterator.next.md)— Переміщує вказівник на одну позицію вперед
-   [ParentIterator::rewind](parentiterator.rewind.md) \- Перекладає ітератор на початок
