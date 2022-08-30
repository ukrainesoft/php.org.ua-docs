Клас IteratorIterator

-   [« InfiniteIterator::next](infiniteiterator.next.html)
    
-   [IteratorIterator::construct »](iteratoriterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Ітератори](spl.iterators.html)
    
-   Клас IteratorIterator
    

# Клас IteratorIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Цей ітератор-обгортка дозволяє перетворювати все, що є "обхідним" ([Traversable](class.traversable.html)) в ітератор. Важливо розуміти, що більшість класів, які не реалізують ітератори, мають на те причини, оскільки швидше за все вони не дозволяють реалізувати повний набір можливостей ітератора. Якщо так, то повинні бути вжиті заходи для запобігання неправильному використанню, інакше очікується винятків або фатальних помилок.

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

> **Зауваження**
> 
> Цей клас дозволяє доступ до методів внутрішнього ітератора через магічний метод call.

## Зміст

-   [IteratorIterator::construct](iteratoriterator.construct.html) — Створює ітератор із чогось, що є обхідним (traversable)
-   [IteratorIterator::current](iteratoriterator.current.html) — Отримує поточне значення
-   [IteratorIterator::getInnerIterator](iteratoriterator.getinneriterator.html) — Отримує внутрішній ітератор
-   [IteratorIterator::key](iteratoriterator.key.html) — Отримує ключ поточного елемента
-   [IteratorIterator::next](iteratoriterator.next.html) — Переміщує ітератор до наступного елементу
-   [IteratorIterator::rewind](iteratoriterator.rewind.html) — Повертає ітератор до першого елементу
-   [IteratorIterator::valid](iteratoriterator.valid.html) — Перевіряє, чи є ітератор допустимим