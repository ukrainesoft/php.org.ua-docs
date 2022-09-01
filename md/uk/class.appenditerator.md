---
navigation:
  - spl.iterators.html: « Ітератори
  - appenditerator.append.html: 'AppendIterator::append »'
  - index.html: PHP Manual
  - spl.iterators.html: Ітератори
title: Клас AppendIterator
---
# Клас AppendIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Ітератор, який виконує кілька інших ітераторів один за одним

## Огляд класів

```classsynopsis

     
    

    
     
      class AppendIterator
     

     
      extends
       IteratorIterator
     
     {

    /* Методы */
    
   public __construct()

    public append(Iterator $iterator): void
public current(): mixed
public getArrayIterator(): ArrayIterator
public getInnerIterator(): Iterator
public getIteratorIndex(): ?int
public key(): scalar
public next(): void
public rewind(): void
public valid(): bool


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

-   [AppendIterator::append](appenditerator.append.html) — додає ітератор
-   [AppendIterator::construct](appenditerator.construct.html) - Створює AppendIterator
-   [AppendIterator::current](appenditerator.current.html) — Повертає поточне значення
-   [AppendIterator::getArrayIterator](appenditerator.getarrayiterator.html) - Повертає клас ітератора масиву ArrayIterator
-   [AppendIterator::getInnerIterator](appenditerator.getinneriterator.html) - Повертає внутрішній ітератор
-   [AppendIterator::getIteratorIndex](appenditerator.getiteratorindex.html) - Повертає індекс ітератора
-   [AppendIterator::key](appenditerator.key.html) — Повертає поточний ключ
-   [AppendIterator::next](appenditerator.next.html) — Переходить до наступного елементу
-   [AppendIterator::rewind](appenditerator.rewind.html) - Перемотує ітератор
-   [AppendIterator::valid](appenditerator.valid.html) — Перевіряє термін дії поточного елемента
