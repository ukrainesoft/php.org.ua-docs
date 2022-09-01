---
navigation:
  - mongodb-driver-server.isarbiter.html: '« MongoDBDriverServer::isArbiter'
  - mongodb-driver-server.ispassive.html: 'MongoDBDriverServer::isPassive »'
  - index.html: PHP Manual
  - class.mongodb-driver-server.html: MongoDBDriverServer
title: 'MongoDBDriverServer::isHidden'
---
# MongoDBDriverServer::isHidden

(mongodb >=1.0.0)

MongoDBDriverServer::isHidden — Перевіряє, чи є сервер прихованим членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isHidden(): bool
```

Повертає, чи є цей сервер [» прихованим членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-hidden-member) набір реплік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є прихованим членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер
