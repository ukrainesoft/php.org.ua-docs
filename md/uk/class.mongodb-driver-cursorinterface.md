---
navigation:
  - mongodb-driver-cursorid.unserialize.md: '« MongoDB\\Driver\\CursorId::unserialize'
  - mongodb-driver-cursorinterface.getid.md: 'MongoDB\\Driver\\CursorInterface::getId »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Інтерфейс MongoDB\\Driver\\CursorInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\Driver\\CursorInterface

(mongodb >=1.6.0)

## Вступ

Інтерфейс, реалізований [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis


    
    
     
      class MongoDB\Driver\CursorInterface
     

     implements 
       Traversable {
    

    /* Методы */
    
   abstract public getId(): MongoDB\Driver\CursorId
abstract public getServer(): MongoDB\Driver\Server
abstract public isDead(): bool
abstract public setTypeMap(array $typemap): void
abstract public toArray(): array

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\Driver\\CursorInterface::getId](mongodb-driver-cursorinterface.getid.md)— Повертає ідентифікатор курсору
-   [MongoDB\\Driver\\CursorInterface::getServer](mongodb-driver-cursorinterface.getserver.md)— Повертає сервер, з яким пов'язаний курсор
-   [MongoDB\\Driver\\CursorInterface::isDead](mongodb-driver-cursorinterface.isdead.md)— Перевірити, чи можна ще отримати з курсору результати
-   [MongoDB\\Driver\\CursorInterface::setTypeMap](mongodb-driver-cursorinterface.settypemap.md)— Задати порівняння типів для десеріалізації BSON
-   [MongoDB\\Driver\\CursorInterface::toArray](mongodb-driver-cursorinterface.toarray.md)— Повернути всі результати для цього курсору у вигляді масиву
