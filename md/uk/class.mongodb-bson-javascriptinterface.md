---
navigation:
  - mongodb-bson-decimal128interface.tostring.html: '« MongoDBBSONDecimal128Interface::toString'
  - mongodb-bson-javascriptinterface.getcode.html: 'MongoDBBSONJavascriptInterface::getCode »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Інтерфейс MongoDBBSONJavascriptInterface
---
# Інтерфейс MongoDBBSONJavascriptInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDBBSONJavascript](class.mongodb-bson-javascript.html), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

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

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBBSONJavascriptInterface::getCode](mongodb-bson-javascriptinterface.getcode.html) — Повертає код JavascriptInterface
-   [MongoDBBSONJavascriptInterface::getScope](mongodb-bson-javascriptinterface.getscope.html) — Повертає область видимості документа JavascriptInterface
-   [MongoDBBSONJavascriptInterface::toString](mongodb-bson-javascriptinterface.tostring.html) — Повертає код JavascriptInterface
