---
navigation:
  - class.mongodb-bson-int64.md: « MongoDB\\BSON\\Int64
  - mongodb-bson-int64.jsonserialize.md: 'MongoDB\\BSON\\Int64::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-int64.md: MongoDB\\BSON\\Int64
title: 'MongoDB\\BSON\\Int64::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Int64::\_\_construct

(mongodb >=1.5.0)

MongoDB\\BSON\\Int64::\_\_construct — Створює новий Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::__construct(int|string $value)
```

Створює новий екземпляр [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)для заданного целого числа.

### Список параметрів

`value`(int|string)

Значення, яке присвоюється екземпляру **Int64**. Це значення може бути надано як ціле число (int) або рядок (string), останнє потрібно на 32-бітових платформах для представлення 64-бітових значень.

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.16.0 |  |
| Метод став доступним для підтримки створення екземплярів Int64 під час роботи з необробленим BSON. |  |

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо рядок `value`не може бути розібрана як 64-бітове ціле число.

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
