---
navigation:
  - mongodb-driver-server.ishidden.html: '« MongoDBDriverServer::isHidden'
  - mongodb-driver-server.isprimary.html: 'MongoDBDriverServer::isPrimary »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.html: MongoDBDriverServer
title: 'MongoDBDriverServer::isPassive'
---
# MongoDBDriverServer::isPassive

(mongodb >=1.0.0)

MongoDBDriverServer::isPassive — Перевіряє, чи є сервер пасивним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isPassive(): bool
```

Повертає, чи є цей сервер [»пасивним членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-passive-member) набору реплік (тобто його пріоритет дорівнює `0`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є пасивним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.md) - Повертає масив інформації, що описує сервер
