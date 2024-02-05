---
navigation:
  - mongodb-bson-dbpointer.unserialize.md: '« MongoDB\\BSON\\DBPointer::unserialize'
  - mongodb-bson-int64.construct.md: 'MongoDB\\BSON\\Int64::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Int64
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Int64

(mongodb >=1.5.0)

## Вступ

Тип BSON для 64-розрядного цілого числа. При декодуванні BSON в PHP цей клас використовується, коли 64-бітове ціле число не може бути представлене як ціле число PHP на 32-бітових платформах. Ці об'єкти підтримують перевантажені [арифметичні](language.operators.arithmetic.md) [побітові](language.operators.bitwise.md) оператори та [оператори порівняння](language.operators.comparison.md)

При роботі з необробленими BSON даними за допомогою класів [MongoDB\\BSON\\Document](class.mongodb-bson-document.md) [MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md) і [MongoDB\\BSON\\Iterator](class.mongodb-bson-iterator.md), будь-яке 64-бітове ціле число буде повернуто як екземпляр цього класу, незалежно від платформи і того, чи може значення бути представлене як ціле число PHP. Це гарантує, що значення можуть бути передані по колу без зміни типу.

Під час кодування BSON об'єкти цього класу будуть перетворені назад у 64-бітовий цілий тип, навіть якщо значення поміщається в 32-бітове ціле число. Це дозволяє явно зберігати значення як 64-бітові цілі числа у BSON.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\BSON\Int64
     

     implements 
       MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {


    /* Методы */
    
   final public __construct(int|string $value)
final public jsonSerialize(): mixed
final public serialize(): string
final public __toString(): string
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.16.0 | Тепер клас може бути ініціалізований на всіх платформах. Додано підтримку перевантажених арифметичних, побітових операторів та операторів порівняння. |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |

## Зміст

-   [MongoDB\\BSON\\Int64::\_\_construct](mongodb-bson-int64.construct.md) \- Створює новий Int64
-   [MongoDB\\BSON\\Int64::jsonSerialize](mongodb-bson-int64.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Int64::serialize](mongodb-bson-int64.serialize.md) \- Серіалізує Int64
-   [MongoDB\\BSON\\Int64::\_\_function toString() { \[native code\] }](mongodb-bson-int64.tostring.md)— Повертає рядкову виставу Int64
-   [MongoDB\\BSON\\Int64::unserialize](mongodb-bson-int64.unserialize.md) \- Десеріалізує Int64
