Клас MongoDBBSONDecimal128

-   [« MongoDBBSONBinary::unserialize](mongodb-bson-binary.unserialize.html)
    
-   [MongoDBBSONDecimal128::construct »](mongodb-bson-decimal128.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSON](book.bson.html)
    
-   Клас MongoDBBSONDecimal128
    

# Клас MongoDBBSONDecimal128

(mongodb >=1.2.0)

## Вступ

Тип BSON для [» Decimal128 формата с плавающей точкой](https://en.wikipedia.org/wiki/Decimal128_floating-point_format), який підтримує числа до 34 десяткових знаків (тобто значних цифр) і діапазон експонентів від -6143 до +6144.

На відміну від типу double BSON (тобто float у PHP), який зберігає лише приблизні значення десяткових значень, тип даних decimal зберігає точне значення. Наприклад, `MongoDB\BSON\Decimal128('9.99')` має точне значення 9-99, де подвійне значення 9-99 буде мати приблизне значення 9.9900000000000002131628….

> **Зауваження** **MongoDBBSONDecimal128** сумісний лише з MongoDB 3.4+. При спробі використовувати тип BSON з попередніми версіями приведе до помилки.

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
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+. |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDBBSONDecimal128Interface](class.mongodb-bson-decimal128interface.html) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html) |

## Зміст

-   [MongoDBBSONDecimal128::construct](mongodb-bson-decimal128.construct.html) - Створює новий Decimal128
-   [MongoDBBSONDecimal128::jsonSerialize](mongodb-bson-decimal128.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONDecimal128::serialize](mongodb-bson-decimal128.serialize.html) - Серіалізує Decimal128
-   [MongoDBBSONDecimal128::toString](mongodb-bson-decimal128.tostring.html) — Повертає рядкову виставу Decimal128
-   [MongoDBBSONDecimal128::unserialize](mongodb-bson-decimal128.unserialize.html) - Десеріалізує Decimal128