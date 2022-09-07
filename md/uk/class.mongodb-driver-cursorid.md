---
navigation:
  - mongodb-driver-cursor.valid.md: '« MongoDBDriverCursor::valid'
  - mongodb-driver-cursorid.construct.md: 'MongoDBDriverCursorId::construct »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDBDriver
title: Клас MongoDBDriverCursorId
---
# Клас MongoDBDriverCursorId

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverCursorID** - Об'єкт значення, який представляє ідентифікатор курсору. Примірники цього класу повертаються [MongoDBDriverCursor::getId()](mongodb-driver-cursor.getid.md)

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
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.7.0 | Реалізує [Serializable](class.serializable.md) |

## Зміст

-   [MongoDBDriverCursorId::construct](mongodb-driver-cursorid.construct.md) — Створює новий об'єкт CursorId (не використовується)
-   [MongoDBDriverCursorId::serialize](mongodb-driver-cursorid.serialize.md) - Серіалізація CursorId
-   [MongoDBDriverCursorId::toString](mongodb-driver-cursorid.tostring.md) - Строкове подання ідентифікатора курсора
-   [MongoDBDriverCursorId::unserialize](mongodb-driver-cursorid.unserialize.md) - Десеріалізація CursorId
