---
navigation:
  - iteratoraggregate.getiterator.md: '« IteratorAggregate::getIterator'
  - internaliterator.construct.md: 'InternalIterator::\_\_construct »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Клас InternalIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас InternalIterator

(PHP 8)

## Вступ

Класс для упрощения реализации интерфейса[IteratorAggregate](class.iteratoraggregate.md)для*внутрішніх* класів.

## Огляд класів

```classsynopsis

    
     final
     class InternalIterator
    

    
     implements
      Iterator {

    /* Методы */
    
   private __construct()

    public current(): mixed
public key(): mixed
public next(): void
public rewind(): void
public valid(): bool

   }
```

## Зміст

-   [InternalIterator::\_\_construct](internaliterator.construct.md)— Закритий конструктор для заборони прямої ініціалізації
-   [InternalIterator::current](internaliterator.current.md)— Повертає поточний елемент
-   [InternalIterator::key](internaliterator.key.md)— Повертає ключ поточного елемента
-   [InternalIterator::next](internaliterator.next.md)— Переходить до наступного елементу
-   [InternalIterator::rewind](internaliterator.rewind.md) \- Перемотує ітератор до першого елементу
-   [InternalIterator::valid](internaliterator.valid.md)— Перевіряє, чи дійсна позиція дійсна
