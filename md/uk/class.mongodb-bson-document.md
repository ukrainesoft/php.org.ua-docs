---
navigation:
  - function.mongodb.bson-torelaxedextendedjson.md: « MongoDB\\BSON\\toRelaxedExtendedJSON
  - mongodb-bson-document.construct.md: 'MongoDB\\BSON\\Document::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Document
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Document

(mongodb >=1.16.0)

## Вступ

Подає BSON-документ. Клас використовується для читання даних у вигляді необробленого BSON і не може бути модифікований.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\BSON\Document
     

     implements 
       MongoDB\BSON\Type,  IteratorAggregate,  Serializable {
    

    /* Методы */
    
   final private __construct()
final static public fromBSON(string $bson): MongoDB\BSON\Document
final static public fromJSON(string $json): MongoDB\BSON\Document
final static public fromPHP(object|array $value): MongoDB\BSON\Document
final public get(string $key): mixed
final public getIterator(): MongoDB\BSON\Iterator
final public has(string $key): bool
final public serialize(): string
final public toCanonicalExtendedJSON(): string
final public toPHP(?array $typeMap = null): array|object
final public toRelaxedExtendedJSON(): string
final public __toString(): string
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.17.0 | Реалізує [MongoDB\\BSON\\Type](class.mongodb-bson-type.md) |

## Зміст

-   [MongoDB\\BSON\\Document::\_\_construct](mongodb-bson-document.construct.md)— Створює новий документ BSON (не використовується)
-   [MongoDB\\BSON\\Document::fromBSON](mongodb-bson-document.frombson.md)— Створює новий екземпляр документа з BSON-рядку
-   [MongoDB\\BSON\\Document::fromJSON](mongodb-bson-document.fromjson.md)— Створює новий екземпляр документа з рядка JSON
-   [MongoDB\\BSON\\Document::fromPHP](mongodb-bson-document.fromphp.md)— Створює новий екземпляр документа з даних PHP
-   [MongoDB\\BSON\\Document::get](mongodb-bson-document.get.md)— Повертає значення ключа у документі
-   [MongoDB\\BSON\\Document::getIterator](mongodb-bson-document.getiterator.md)— Повертає ітератор для документа BSON
-   [MongoDB\\BSON\\Document::has](mongodb-bson-document.has.md)— Повертає, чи є ключ у документі
-   [MongoDB\\BSON\\Document::serialize](mongodb-bson-document.serialize.md) \- Серіалізує документ
-   [MongoDB\\BSON\\Document::toCanonicalExtendedJSON](mongodb-bson-document.tocanonicalextendedjson.md)— Повертає Canonical Extended JSON-подання BSON-документу
-   [MongoDB\\BSON\\Document::toPHP](mongodb-bson-document.tophp.md)— Повертає PHP-подання документа BSON
-   [MongoDB\\BSON\\Document::toRelaxedExtendedJSON](mongodb-bson-document.torelaxedextendedjson.md)— Повертає Relaxed Extended JSON подання BSON-документу
-   [MongoDB\\BSON\\Document::\_\_function toString() { \[native code\] }](mongodb-bson-document.tostring.md)— Повертає строкове подання цього BSON-документу
-   [MongoDB\\BSON\\Document::unserialize](mongodb-bson-document.unserialize.md) \- Десеріалізує BSON-документ
