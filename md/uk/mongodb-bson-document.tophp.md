---
navigation:
  - mongodb-bson-document.tocanonicalextendedjson.md: '« MongoDB\\BSON\\Document::toCanonicalExtendedJSON'
  - mongodb-bson-document.torelaxedextendedjson.md: 'MongoDB\\BSON\\Document::toRelaxedExtendedJSON »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::toPHP'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::toPHP

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::toPHP — Повертає PHP-подання документа BSON

### Опис

```methodsynopsis
final public MongoDB\BSON\Document::toPHP(?array $typeMap = null): array|object
```

Десериализует BSON-документ в его PHP-представление. Параметр`typeMap` може бути використаний для керування типами PHP, що використовуються для перетворення BSON-масивів та документів (як кореневих, так і вбудованих).

**Увага**

Документи BSON технічно можуть містити ключі, що повторюються, оскільки документи зберігаються у вигляді списку пар ключ-значення; однак програмам слід утримуватися від створення документів з дублікатами ключів, оскільки поведінка сервера та драйвера може бути невизначеною. Оскільки об'єкти та масиви PHP не можуть мати ключів, що повторюються, дані також можуть бути втрачені при декодуванні документа BSON з повторюваними ключами.

### Список параметрів

`typeMap`(array)

[Конфігурація карти типів](mongodb.persistence.deserialization.md#mongodb.persistence.typemaps)

### Значення, що повертаються

Десеріалізоване PHP значення.

> **Зауваження**: Якщо в BSON-документі зустрічається значення, закодоване як 64-бітове ціле число, то значенням, що повертається, буде екземпляр [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)

### Помилки

-   Викидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо клас у карті типів не може бути ініціалізований або не реалізує інтерфейс[MongoDB\\BSON\\Unserializable](class.mongodb-bson-unserializable.md)

### Дивіться також

-   [MongoDB\\BSON\\toPHP()](function.mongodb.bson-tophp.md) \- Повертає PHP подання значення BSON
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
