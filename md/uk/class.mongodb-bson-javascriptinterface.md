---
navigation:
  - mongodb-bson-decimal128interface.tostring.md: >-
      « MongoDB\\BSON\\Decimal128Interface::\_\_function toString() { [native
      code] }
  - mongodb-bson-javascriptinterface.getcode.md: 'MongoDB\\BSON\\JavascriptInterface::getCode »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\JavascriptInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\JavascriptInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis

    
     
      class MongoDB\BSON\JavascriptInterface
     
     {
    /* Методы */
    
   abstract public getCode(): string
abstract public getScope(): ?object
abstract public __toString(): string

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\JavascriptInterface::getCode](mongodb-bson-javascriptinterface.getcode.md)— Повертає код JavascriptInterface
-   [MongoDB\\BSON\\JavascriptInterface::getScope](mongodb-bson-javascriptinterface.getscope.md)— Повертає область видимості документа JavascriptInterface
-   [MongoDB\\BSON\\JavascriptInterface::\_\_function toString() { \[native code\] }](mongodb-bson-javascriptinterface.tostring.md)— Повертає код JavascriptInterface
