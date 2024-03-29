---
navigation:
  - filesystemiterator.setflags.md: '« FilesystemIterator::setFlags'
  - filteriterator.accept.md: 'FilterIterator::accept »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас FilterIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас FilterIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Цей абстрактний ітератор відфільтровує небажані значення. Цей клас слід розширити для реалізації фільтрів ітератора. Метод [FilterIterator::accept()](filteriterator.accept.md) має бути реалізований у підкласі.

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

-   [FilterIterator::accept](filteriterator.accept.md)— Перевіряє, чи поточний елемент ітератора є допустимим.
-   [FilterIterator::\_\_construct](filteriterator.construct.md) \- Конструктор класу FilterIterator
-   [FilterIterator::current](filteriterator.current.md)— Отримує значення поточного елемента
-   [FilterIterator::key](filteriterator.key.md)— Отримує поточний ключ
-   [FilterIterator::next](filteriterator.next.md)— Переміщує ітератор до наступного елемента
-   [FilterIterator::rewind](filteriterator.rewind.md)— Повертає ітератор на початок
-   [FilterIterator::valid](filteriterator.valid.md)— Перевіряє, чи поточний елемент є допустимим
