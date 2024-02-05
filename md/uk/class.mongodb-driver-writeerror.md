---
navigation:
  - mongodb-driver-writeconcernerror.getmessage.md: '« MongoDB\\Driver\\WriteConcernError::getMessage'
  - mongodb-driver-writeerror.getcode.md: 'MongoDB\\Driver\\WriteError::getCode »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\WriteError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\WriteError

(mongodb >=1.0.0)

## Вступ

Класс**MongoDB\\Driver\\WriteError** інкапсулює інформацію про помилку запису і може бути повернутий як елемент масиву з [MongoDB\\Driver\\WriteResult::getWriteErrors()](mongodb-driver-writeresult.getwriteerrors.md)

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\WriteError
     
     {


    /* Методы */
    
   final public getCode(): int
final public getIndex(): int
final public getInfo(): ?object
final public getMessage(): string

   }
```

## Зміст

-   [MongoDB\\Driver\\WriteError::getCode](mongodb-driver-writeerror.getcode.md)— Повертає код помилки WriteError
-   [MongoDB\\Driver\\WriteError::getIndex](mongodb-driver-writeerror.getindex.md)— Повертає індекс запису, який відповідає цьому WriteError
-   [MongoDB\\Driver\\WriteError::getInfo](mongodb-driver-writeerror.getinfo.md)— Повертає документ метаданих для WriteError
-   [MongoDB\\Driver\\WriteError::getMessage](mongodb-driver-writeerror.getmessage.md)— Повертає повідомлення про помилку WriteError
