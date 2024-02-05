---
navigation:
  - mongodb-driver-server.getserverdescription.md: '« MongoDB\\Driver\\Server::getServerDescription'
  - mongodb-driver-server.gettype.md: 'MongoDB\\Driver\\Server::getType »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::getTags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::getTags

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::getTags — Повертає масив тегів, що описують сервер у наборі реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getTags(): array
```

Повертає array [» тегів](https://www.mongodb.com/docs/manual/reference/glossary/#term-tag), що використовуються для опису цього сервера в наборі реплік. Масив буде містити нуль або більше пар string ключів та значень.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає array теги, що використовуються для опису сервера в наборі реплік.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
