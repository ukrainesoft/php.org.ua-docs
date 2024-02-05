---
navigation:
  - function.mongodb.bson-fromjson.md: « MongoDB\\BSON\\fromJSON
  - function.mongodb.bson-tocanonicalextendedjson.md: MongoDB\\BSON\\toCanonicalExtendedJSON »
  - index.md: PHP Manual
  - ref.bson.functions.md: Функції
title: MongoDB\\BSON\\fromPHP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\fromPHP

(mongodb >=1.0.0)

MongoDB\\BSON\\fromPHP — Повертає представлення BSON значення PHP

### Опис

```methodsynopsis
MongoDB\BSON\fromPHP(array|object $value): string
```

Серіалізує масив або об'єкт PHP (наприклад, документ) для його подання [» BSON](https://www.mongodb.com/docs/manual/reference/bson-types/). Повернутий двійковий рядок буде описувати документ BSON.

### Список параметрів

`value`(array|object)

Значення PHP для серіалізації.

### Значення, що повертаються

Серіалізований документ BSON у вигляді двійкового рядка.

### Помилки

-   Видає[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md), якщо значення PHP не може бути перетворено на BSON. Можливі причини включають, але не обмежуються, зіткненням з несподіваним екземпляром[MongoDB\\BSON\\Type](class.mongodb-bson-type.md) або [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md), не може повернути array або[stdClass](class.stdclass.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\fromPHP()\*\*\*\*

```php
<?php

$bson = MongoDB\BSON\fromPHP(['foo' => 1]);
echo bin2hex($bson), "\n";

?>
```

Результат виконання наведеного прикладу:

```
0e00000010666f6f000100000000cat
```

### Дивіться також

-   [MongoDB\\BSON\\Document::fromPHP()](mongodb-bson-document.fromphp.md) \- Створює новий екземпляр документа з даних PHP
-   [MongoDB\\BSON\\toPHP()](function.mongodb.bson-tophp.md) \- Повертає PHP подання значення BSON
-   [» MongoDB BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
-   [Постійні дані](mongodb.persistence.md)
