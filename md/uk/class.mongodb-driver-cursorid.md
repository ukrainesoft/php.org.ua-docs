---
navigation:
  - mongodb-driver-cursor.valid.md: '« MongoDB\\Driver\\Cursor::valid'
  - mongodb-driver-cursorid.construct.md: 'MongoDB\\Driver\\CursorId::\_\_construct »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\CursorId
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\CursorId

(mongodb >=1.0.0)

## Вступ

Класс**MongoDB\\Driver\\CursorID** - Об'єкт значення, який представляє ідентифікатор курсору. Примірники цього класу повертаються [MongoDB\\Driver\\Cursor::getId()](mongodb-driver-cursor.getid.md)

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\CursorId
     

     implements 
       Serializable,  Stringable {
    

    /* Методы */
    
   final private __construct()
final public serialize(): string
final public __toString(): string
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.7.0 | Реалізує [Serializable](class.serializable.md) |

## Зміст

-   [MongoDB\\Driver\\CursorId::\_\_construct](mongodb-driver-cursorid.construct.md)— Створює новий об'єкт CursorId (не використовується)
-   [MongoDB\\Driver\\CursorId::serialize](mongodb-driver-cursorid.serialize.md) \- Серіалізація CursorId
-   [MongoDB\\Driver\\CursorId::\_\_function toString() { \[native code\] }](mongodb-driver-cursorid.tostring.md)— Строкове подання ідентифікатора курсору
-   [MongoDB\\Driver\\CursorId::unserialize](mongodb-driver-cursorid.unserialize.md) \- Десеріалізація CursorId
