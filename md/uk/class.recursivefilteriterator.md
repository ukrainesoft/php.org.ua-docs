Клас RecursiveFilterIterator

-   [« RecursiveDirectoryIterator::rewind](recursivedirectoryiterator.rewind.html)
    
-   [RecursiveFilterIterator::construct »](recursivefilteriterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Ітератори](spl.iterators.html)
    
-   Клас RecursiveFilterIterator
    

# Клас RecursiveFilterIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Цей абстрактний ітератор відфільтровує небажані значення для [RecursiveIterator](class.recursiveiterator.html). Цей клас слід розширювати для реалізації фільтрів користувача. Метод **RecursiveFilterIterator::accept()** необхідно реалізовувати у підкласі.

## Огляд класів

```classsynopsis

     
    

    
     
      abstract
      class RecursiveFilterIterator
     

     
      extends
       FilterIterator
     

     implements 
       RecursiveIterator {

    /* Методы */
    
   public __construct(RecursiveIterator $iterator)

    public getChildren(): ?RecursiveFilterIterator
public hasChildren(): bool


    /* Наследуемые методы */
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

-   [RecursiveFilterIterator::construct](recursivefilteriterator.construct.html) — Створює об'єкт RecursiveFilterIterator на основі об'єкта-ітератора RecursiveIterator
-   [RecursiveFilterIterator::getChildren](recursivefilteriterator.getchildren.html) — Повертає дочірні елементи внутрішнього ітератора як об'єкт RecursiveFilterIterator
-   [RecursiveFilterIterator::hasChildren](recursivefilteriterator.haschildren.html) — Перевіряє, чи має поточний елемент внутрішнього ітератора дочірні елементи.