---
navigation:
  - mongodb-bson-packedarray.unserialize.md: '« MongoDB\\BSON\\PackedArray::unserialize'
  - mongodb-bson-iterator.construct.md: 'MongoDB\\BSON\\Iterator::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Iterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Iterator

(mongodb >=1.16.0)

## Вступ

Ітератор, що використовується для обходу документа BSON або масиву.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\BSON\Iterator
     

     implements 
       Iterator {
    

    /* Методы */
    
   final private __construct()
public current(): mixed
public key(): string|int
public next(): void
public rewind(): void
public valid(): bool

   }
```

## Зміст

-   [MongoDB\\BSON\\Iterator::\_\_construct](mongodb-bson-iterator.construct.md)— Створює новий ітератор BSON (не використовується)
-   [MongoDB\\BSON\\Iterator::current](mongodb-bson-iterator.current.md)— Повертає поточний елемент
-   [MongoDB\\BSON\\Iterator::key](mongodb-bson-iterator.key.md)— Повертає ключ поточного елемента
-   [MongoDB\\BSON\\Iterator::next](mongodb-bson-iterator.next.md)— Переміщує ітератор до наступного елемента
-   [MongoDB\\BSON\\Iterator::rewind](mongodb-bson-iterator.rewind.md) \- Перемотує ітератор до першого елементу
-   [MongoDB\\BSON\\Iterator::valid](mongodb-bson-iterator.valid.md)— Перевіряє, чи поточна позиція є коректною.
