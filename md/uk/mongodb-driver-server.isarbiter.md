---
navigation:
  - mongodb-driver-server.gettype.md: '« MongoDB\\Driver\\Server::getType'
  - mongodb-driver-server.ishidden.md: 'MongoDB\\Driver\\Server::isHidden »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::isArbiter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::isArbiter

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::isArbiter — Перевіряє, чи є сервер членом-арбітром у наборі реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isArbiter(): bool
```

Повертає, чи є цей сервер [» членом-арбітром](https://www.mongodb.com/docs/manual/reference/glossary/#term-arbiter)набора реплик.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є членом-арбітром набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
