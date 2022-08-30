Клас MongoDBDriverCursorId

-   [« MongoDBDriverCursor::valid](mongodb-driver-cursor.valid.html)
    
-   [MongoDBDriverCursorId::construct »](mongodb-driver-cursorid.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriver](book.mongodb.html)
    
-   Клас MongoDBDriverCursorId
    

# Клас MongoDBDriverCursorId

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverCursorID** - Об'єкт значення, який представляє ідентифікатор курсору. Примірники цього класу повертаються [MongoDBDriverCursor::getId()](mongodb-driver-cursor.getid.html)

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

| Версия              | Описание                                                             |
|---------------------|----------------------------------------------------------------------|
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+. |
| PECL mongodb 1.7.0  | Реалізує [Serializable](class.serializable.html)                     |

## Зміст

-   [MongoDBDriverCursorId::construct](mongodb-driver-cursorid.construct.html) — Створює новий об'єкт CursorId (не використовується)
-   [MongoDBDriverCursorId::serialize](mongodb-driver-cursorid.serialize.html) - Серіалізація CursorId
-   [MongoDBDriverCursorId::toString](mongodb-driver-cursorid.tostring.html) - Строкове подання ідентифікатора курсора
-   [MongoDBDriverCursorId::unserialize](mongodb-driver-cursorid.unserialize.html) - Десеріалізація CursorId