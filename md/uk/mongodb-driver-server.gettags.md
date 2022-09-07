---
navigation:
  - mongodb-driver-server.getserverdescription.md: '« MongoDBDriverServer::getServerDescription'
  - mongodb-driver-server.gettype.md: 'MongoDBDriverServer::getType »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::getTags'
---
# MongoDBDriverServer::getTags

(mongodb >=1.0.0)

MongoDBDriverServer::getTags — Повертає масив тегів, що описують сервер у наборі реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getTags(): array
```

Повертає array [»тегів](https://www.mongodb.com/docs/manual/reference/glossary/#term-tag), що використовуються для опису цього сервера в наборі реплік. Масив буде містити нуль або більше пар string ключів та значень.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає array теги, що використовуються для опису сервера в наборі реплік.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.md) - Повертає масив інформації, що описує сервер
