---
navigation:
  - spl.iterators.md: « Ітератори
  - appenditerator.append.md: 'AppendIterator::append »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
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

-   [AppendIterator::append](appenditerator.append.md) — додає ітератор
-   [AppendIterator::construct](appenditerator.construct.md) - Створює AppendIterator
-   [AppendIterator::current](appenditerator.current.md) — Повертає поточне значення
-   [AppendIterator::getArrayIterator](appenditerator.getarrayiterator.md) - Повертає клас ітератора масиву ArrayIterator
-   [AppendIterator::getInnerIterator](appenditerator.getinneriterator.md) - Повертає внутрішній ітератор
-   [AppendIterator::getIteratorIndex](appenditerator.getiteratorindex.md) - Повертає індекс ітератора
-   [AppendIterator::key](appenditerator.key.md) — Повертає поточний ключ
-   [AppendIterator::next](appenditerator.next.md) — Переходить до наступного елементу
-   [AppendIterator::rewind](appenditerator.rewind.md) - Перемотує ітератор
-   [AppendIterator::valid](appenditerator.valid.md) — Перевіряє термін дії поточного елемента
