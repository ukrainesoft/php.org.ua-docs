---
navigation:
  - mongodb-bson-binary.unserialize.md: '« MongoDB\\BSON\\Binary::unserialize'
  - mongodb-bson-decimal128.construct.md: 'MongoDB\\BSON\\Decimal128::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Decimal128
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Decimal128

(mongodb >=1.2.0)

## Вступ

Тип BSON для[» Decimal128 формату з плаваючою точкою](https://en.wikipedia.org/wiki/Decimal128_floating-point_format), який підтримує числа до 34 десяткових знаків (тобто значних цифр) і діапазон експонентів від -6143 до +6144.

На відміну від типу double BSON (тобто float у PHP), який зберігає лише приблизні значення десяткових значень, тип даних decimal зберігає точне значення. Наприклад, `MongoDB\BSON\Decimal128('9.99')` має точне значення 9-99, де подвійне значення 9-99 буде мати приблизне значення 9.9900000000000002131628….

> **Зауваження** **MongoDB\\BSON\\Decimal128** сумісний лише з MongoDB 3.4+. При спробі використовувати тип BSON з попередніми версіями приведе до помилки.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\BSON\Decimal128
     

     implements 
       MongoDB\BSON\Decimal128Interface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {
    

    /* Методы */
    
   final public __construct(string $value)
final public jsonSerialize(): mixed
final public serialize(): string
final public __toString(): string
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDB\\BSON\\Decimal128Interface](class.mongodb-bson-decimal128interface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDB\\BSON\\Decimal128::\_\_construct](mongodb-bson-decimal128.construct.md) \- Створює новий Decimal128
-   [MongoDB\\BSON\\Decimal128::jsonSerialize](mongodb-bson-decimal128.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Decimal128::serialize](mongodb-bson-decimal128.serialize.md) \- Серіалізує Decimal128
-   [MongoDB\\BSON\\Decimal128::\_\_function toString() { \[native code\] }](mongodb-bson-decimal128.tostring.md)— Повертає рядкову виставу Decimal128
-   [MongoDB\\BSON\\Decimal128::unserialize](mongodb-bson-decimal128.unserialize.md) \- Десеріалізує Decimal128
