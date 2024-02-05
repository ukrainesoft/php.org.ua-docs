---
navigation:
  - mongodb-driver-server.ispassive.md: '« MongoDB\\Driver\\Server::isPassive'
  - mongodb-driver-server.issecondary.md: 'MongoDB\\Driver\\Server::isSecondary »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::isPrimary'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::isPrimary

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::isPrimary — Перевіряє, чи є сервер основним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isPrimary(): bool
```

Повертає, чи є цей сервер [»основним членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-primary)набора реплик.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є основним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
