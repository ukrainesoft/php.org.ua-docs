Клас MongoDBBSONInt64

-   [« MongoDBBSONDBPointer::unserialize](mongodb-bson-dbpointer.unserialize.html)
    
-   [MongoDBBSONInt64::construct »](mongodb-bson-int64.construct.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSON](book.bson.md)
    
-   Клас MongoDBBSONInt64
    

# Клас MongoDBBSONInt64

(mongodb >=1.5.0)

## Вступ

Тип BSON для 64-розрядного цілого числа. Цей клас не може бути створений і створюється тільки під час декодування BSON, коли 64-розрядне ціле не може бути представлене як ціле число PHP на 32-розрядній платформі. Версії драйвера до 1.5.0 викличуть виняток у разі спроби декодування 64-розрядного цілого числа на 32-розрядній платформі.

Під час кодування BSON об'єкти цього класу будуть перетворені назад на 64-бітовий цілий тип. Це дозволяє використовувати 64-бітові цілі числа у 32-бітовому середовищі PHP без втрати точності. Метод [toString()](language.oop5.magic.html#object.tostring) дозволяє отримати доступ до 64-бітового цілого значення у вигляді рядка.

> **Зауваження**: Цей клас існує виключно для 32-бітових платформ Програми на 64-бітових платформах (тобто . [**`PHP_INT_SIZE`**](reserved.constants.html#constant.php-int-size) 8) ніколи не повинні стикатися з цим класом під час нормальної роботи.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\BSON\Int64
     

     implements 
       MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {


    /* Методы */
    
   final private __construct()
final public jsonSerialize(): mixed
final public serialize(): string
final public __toString(): string
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия              | Описание                                                           |
|---------------------|--------------------------------------------------------------------|
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |

## Зміст

-   [MongoDBBSONInt64::construct](mongodb-bson-int64.construct.html) — Створює новий Int64 (не використовується)
-   [MongoDBBSONInt64::jsonSerialize](mongodb-bson-int64.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONInt64::serialize](mongodb-bson-int64.serialize.html) - Серіалізує Int64
-   [MongoDBBSONInt64::toString](mongodb-bson-int64.tostring.html) — Повертає рядкову виставу Int64
-   [MongoDBBSONInt64::unserialize](mongodb-bson-int64.unserialize.html) - Десеріалізує Int64