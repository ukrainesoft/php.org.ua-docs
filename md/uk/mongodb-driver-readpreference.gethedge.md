---
navigation:
  - mongodb-driver-readpreference.construct.html: '« MongoDBDriverReadPreference::construct'
  - mongodb-driver-readpreference.getmaxstalenessseconds.html: 'MongoDBDriverReadPreference::getMaxStalenessSeconds »'
  - index.html: PHP Manual
  - class.mongodb-driver-readpreference.html: MongoDBDriverReadPreference
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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [» документация по Read Preference](https://www.mongodb.com/docs/manual/core/read-preference/)
