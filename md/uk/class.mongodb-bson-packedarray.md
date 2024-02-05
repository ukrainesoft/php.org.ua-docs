---
navigation:
  - mongodb-bson-document.unserialize.md: '« MongoDB\\BSON\\Document::unserialize'
  - mongodb-bson-packedarray.construct.md: 'MongoDB\\BSON\\PackedArray::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\PackedArray
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\PackedArray

(mongodb >=1.16.0)

## Вступ

Представляє масив BSON. Клас використовується для читання даних у вигляді необробленого BSON і не може бути модифікований.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\BSON\PackedArray
     

     implements 
       MongoDB\BSON\Type,  IteratorAggregate,  Serializable {
    

    /* Методы */
    
   final private __construct()
final static public fromPHP(array $value): MongoDB\BSON\PackedArray
final public get(int $key): mixed
final public getIterator(): MongoDB\BSON\Iterator
final public has(int $index): bool
final public serialize(): string
final public toPHP(?array $typeMap = null): array|object
final public __toString(): string
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.17.0 | Реалізує [MongoDB\\BSON\\Type](class.mongodb-bson-type.md) |
| PECL mongodb 1.17.0 | Класс**MongoDB\\BSON\\PackedArray** не може бути серіалізований у контекстах, де очікується BSON-документ. У попередніх версіях BSON-масив повинен був бути перетворений на документ. |

## Зміст

-   [MongoDB\\BSON\\PackedArray::\_\_construct](mongodb-bson-packedarray.construct.md) \- Створює новий масив BSON (не використовується)
-   [MongoDB\\BSON\\PackedArray::fromPHP](mongodb-bson-packedarray.fromphp.md)— Створює новий екземпляр масиву BSON із даних PHP
-   [MongoDB\\BSON\\PackedArray::get](mongodb-bson-packedarray.get.md)— Повертає значення індексу масиву
-   [MongoDB\\BSON\\PackedArray::getIterator](mongodb-bson-packedarray.getiterator.md) \- Повертає ітератор для масиву BSON
-   [MongoDB\\BSON\\PackedArray::has](mongodb-bson-packedarray.has.md)— Повертає, чи є індекс у масиві
-   [MongoDB\\BSON\\PackedArray::serialize](mongodb-bson-packedarray.serialize.md) \- Серіалізація масиву BSON
-   [MongoDB\\BSON\\PackedArray::toPHP](mongodb-bson-packedarray.tophp.md)— Повертає PHP-представлення масиву BSON
-   [MongoDB\\BSON\\PackedArray::\_\_function toString() { \[native code\] }](mongodb-bson-packedarray.tostring.md)— Повертає рядкову виставу BSON-масиву
-   [MongoDB\\BSON\\PackedArray::unserialize](mongodb-bson-packedarray.unserialize.md) \- Десеріалізує масив BSON
