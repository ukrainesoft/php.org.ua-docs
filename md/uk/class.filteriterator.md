Клас FilterIterator

-   [« FilesystemIterator::setFlags](filesystemiterator.setflags.html)
    
-   [FilterIterator::accept »](filteriterator.accept.html)
    
-   [PHP Manual](index.html)
    
-   [Ітератори](spl.iterators.html)
    
-   Клас FilterIterator
    

# Клас FilterIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Цей абстрактний ітератор відфільтровує небажані значення. Цей клас слід розширити для реалізації фільтрів ітератора. Метод [FilterIterator::accept()](filteriterator.accept.html) має бути реалізований у підкласі.

## Огляд класів

```classsynopsis

     
    

    
     
      abstract
      class FilterIterator
     

     
      extends
       IteratorIterator
     
     {

    /* Методы */
    
   public __construct(Iterator $iterator)

    public accept(): bool
public current(): mixed
public getInnerIterator(): Iterator
public key(): mixed
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

-   [FilterIterator::accept](filteriterator.accept.html) — Перевіряє, чи поточний елемент ітератора є допустимим.
-   [FilterIterator::construct](filteriterator.construct.html) - Конструктор класу FilterIterator
-   [FilterIterator::current](filteriterator.current.html) — Отримує значення поточного елемента
-   [FilterIterator::getInnerIterator](filteriterator.getinneriterator.html) — Отримує внутрішній ітератор
-   [FilterIterator::key](filteriterator.key.html) — Отримує поточний ключ
-   [FilterIterator::next](filteriterator.next.html) — Переміщує ітератор до наступного елементу
-   [FilterIterator::rewind](filteriterator.rewind.html) — Повертає ітератор на початок
-   [FilterIterator::valid](filteriterator.valid.html) — Перевіряє, чи поточний елемент є допустимим