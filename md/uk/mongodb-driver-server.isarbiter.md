---
navigation:
  - mongodb-driver-server.gettype.md: '« MongoDBDriverServer::getType'
  - mongodb-driver-server.ishidden.md: 'MongoDBDriverServer::isHidden »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::isArbiter'
---
# MongoDBDriverServer::isArbiter

(mongodb >=1.0.0)

MongoDBDriverServer::isArbiter — Перевіряє, чи є сервер членом-арбітром у наборі реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isArbiter(): bool
```

Повертає, чи є цей сервер [» членом-арбітром](https://www.mongodb.com/docs/manual/reference/glossary/#term-arbiter) набір реплік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є членом-арбітром набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.md) - Повертає масив інформації, що описує сервер
