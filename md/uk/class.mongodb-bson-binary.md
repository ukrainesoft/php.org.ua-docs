---
navigation:
  - mongodb-bson-iterator.valid.md: '« MongoDB\\BSON\\Iterator::valid'
  - mongodb-bson-binary.construct.md: 'MongoDB\\BSON\\Binary::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Binary
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Binary

(mongodb >=1.0.0)

## Вступ

Тип BSON для бінарних даних (тобто масиву байт). Бінарні значення також мають підтип, що означає, який тип даних міститься в масиві байт. Підтипи з нуля до 127 визначені або зарезервовані. Підтипи з 128-255 задаються користувачем.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\BSON\Binary
     

     implements 
       MongoDB\BSON\BinaryInterface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {
    
    /* Константы */
    
     const
     int
      TYPE_GENERIC = 0;

    const
     int
      TYPE_FUNCTION = 1;

    const
     int
      TYPE_OLD_BINARY = 2;

    const
     int
      TYPE_OLD_UUID = 3;

    const
     int
      TYPE_UUID = 4;

    const
     int
      TYPE_MD5 = 5;

    const
     int
      TYPE_ENCRYPTED = 6;

    const
     int
      TYPE_COLUMN = 7;

    const
     int
      TYPE_SENSITIVE = 8;

    const
     int
      TYPE_USER_DEFINED = 128;


    /* Методы */
    
   final public __construct(string $data, int $type = MongoDB\BSON\Binary::TYPE_GENERIC)
final public getData(): string
final public getType(): int
final public jsonSerialize(): mixed
final public serialize(): string
final public __toString(): string
final public unserialize(string $data): void

   }
```

## Обумовлені константи

**`MongoDB\BSON\Binary::TYPE_GENERIC`**

Бінарні дані

**`MongoDB\BSON\Binary::TYPE_FUNCTION`**

Функція

**`MongoDB\BSON\Binary::TYPE_OLD_BINARY`**

Бінарні дані (оголошено застарілою, використовуйте **`MongoDB\BSON\Binary::TYPE_GENERIC`**) .

**`MongoDB\BSON\Binary::TYPE_OLD_UUID`**

Універсальний унікальний ідентифікатор (оголошено застарілою. Використовуйте **`MongoDB\BSON\Binary::TYPE_UUID`**). При використанні цього типу, бінарні дані мають бути довжиною 16 байт.

Історично інші значення кодовані цими типами, але іншими драйверами, базуються на інших конвенціях (наприклад, різний тип порядку байт), що робить його непереносним. Драйвер PHP не застосовує жодних обробок для даних цього типу.

**`MongoDB\BSON\Binary::TYPE_UUID`**

Універсальний унікальний ідентифікатор. При використанні цього типу, бінарні дані повинні бути довжиною 16 байт [» RFC 4122](http://www.faqs.org/rfcs/rfc4122)

**`MongoDB\BSON\Binary::TYPE_MD5`**

Хеш MD5. При використанні цього типу, бінарні дані мають бути довжиною 16 байт.

**`MongoDB\BSON\Binary::TYPE_ENCRYPTED`**

Зашифроване значення. Цей тип використовується для шифрування на стороні клієнта.

**`MongoDB\BSON\Binary::TYPE_COLUMN`**

Дані стовпця. Підтип використовується для колекцій часових рядів.

**`MongoDB\BSON\Binary::TYPE_SENSITIVE`**

Конфіденційні дані. Підтип використовується для конфіденційних даних, які, по можливості, повинні бути виключені з логування на стороні сервера.

**`MongoDB\BSON\Binary::TYPE_USER_DEFINED`**

Користувальницький тип. У той час як типи з 0 по 127 визначені, або зарезервовані, типи з 128 по 255 можуть використовуватися для чого завгодно.

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.17.0 | Добавлен тип\*\*`MongoDB\BSON\Binary::TYPE_SENSITIVE`\*\* |
| PECL mongodb 1.12.0 |  |
| Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |  |

Добавлен тип\*\*`MongoDB\BSON\Binary::TYPE_COLUMN`\*\*

| | PECL mongodb 1.7.0 | Добавлен тип\*\*`MongoDB\BSON\Binary::TYPE_ENCRYPTED`\*\*. | | PECL mongodb 1.3.0 Реалізує інтерфейс [MongoDB\\BSON\\BinaryInterface](class.mongodb-bson-binaryinterface.md). | | PECL mongodb 1.2.0 Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md).

## Зміст

-   [MongoDB\\BSON\\Binary::\_\_construct](mongodb-bson-binary.construct.md) \- Створює новий Binary
-   [MongoDB\\BSON\\Binary::getData](mongodb-bson-binary.getdata.md) \- Повертає дані Binary
-   [MongoDB\\BSON\\Binary::getType](mongodb-bson-binary.gettype.md) \- Повертає тип Binary
-   [MongoDB\\BSON\\Binary::jsonSerialize](mongodb-bson-binary.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Binary::serialize](mongodb-bson-binary.serialize.md) \- Серіалізує Binary
-   [MongoDB\\BSON\\Binary::\_\_function toString() { \[native code\] }](mongodb-bson-binary.tostring.md) \- Повертає дані Binary
-   [MongoDB\\BSON\\Binary::unserialize](mongodb-bson-binary.unserialize.md) \- Десеріалізує Binary
