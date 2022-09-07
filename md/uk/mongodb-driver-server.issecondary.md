---
navigation:
  - mongodb-driver-server.isprimary.md: '« MongoDBDriverServer::isPrimary'
  - class.mongodb-driver-serverdescription.md: MongoDBDriverServerDescription »
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::isSecondary'
---
# MongoDBDriverServer::isSecondary

(mongodb >=1.0.0)

MongoDBDriverServer::isSecondary — Перевіряє, чи є сервер другорядним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isSecondary(): bool
```

Повертає, чи є цей сервер [» другорядним членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-secondary) набір реплік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є другорядним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.md) - Повертає масив інформації, що описує сервер
