---
navigation:
  - mongodb-driver-readpreference.construct.md: '« MongoDBDriverReadPreference::construct'
  - mongodb-driver-readpreference.getmaxstalenessseconds.md: 'MongoDBDriverReadPreference::getMaxStalenessSeconds »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDBDriverReadPreference
title: 'MongoDBDriverReadPreference::getHedge'
---
# MongoDBDriverReadPreference::getHedge

(mongodb >=1.8.0)

MongoDBDriverReadPreference::getHedge — Повертає опцію "hedge" із ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getHedge(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "hedge" із ReadPreference.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [» документация по Read Preference](https://www.mongodb.com/docs/manual/core/read-preference/)
