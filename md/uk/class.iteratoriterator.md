---
navigation:
  - infiniteiterator.next.md: '« InfiniteIterator::next'
  - iteratoriterator.construct.md: 'IteratorIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас IteratorIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас IteratorIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Цей ітератор-обгортка дозволяє перетворювати все, що є "обхідним" ([Traversable](class.traversable.md)) в ітератор. Важливо розуміти, що більшість класів, які не реалізують ітератори, мають на те причини, оскільки швидше за все вони не дозволяють реалізувати повний набір можливостей ітератора. Якщо так, то повинні бути вжиті заходи для запобігання неправильному використанню, інакше очікується винятків або фатальних помилок.

## Огляд класів

```classsynopsis

    
     class IteratorIterator
    

    
     implements
      OuterIterator {

    /* Методы */
    
   public __construct(Traversable $iterator, ?string $class = null)

    public current(): mixed
public getInnerIterator(): ?Iterator
public key(): mixed
public next(): void
public rewind(): void
public valid(): bool

   }
```

## Примітки

> **Зауваження** :
> 
> Цей клас дозволяє доступ до методів внутрішнього ітератора через магічний метод \_\_call.

## Зміст

-   [IteratorIterator::\_\_construct](iteratoriterator.construct.md)— Створює ітератор із чогось, що є обхідним (traversable)
-   [IteratorIterator::current](iteratoriterator.current.md)— Отримує поточне значення
-   [IteratorIterator::getInnerIterator](iteratoriterator.getinneriterator.md)— Отримує внутрішній ітератор
-   [IteratorIterator::key](iteratoriterator.key.md)— Отримує ключ поточного елемента
-   [IteratorIterator::next](iteratoriterator.next.md)— Переміщує ітератор до наступного елемента
-   [IteratorIterator::rewind](iteratoriterator.rewind.md)— Повертає ітератор до першого елементу
-   [IteratorIterator::valid](iteratoriterator.valid.md)— Перевіряє, чи є ітератор допустимим
