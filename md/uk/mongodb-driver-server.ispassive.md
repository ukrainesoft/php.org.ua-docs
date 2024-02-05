---
navigation:
  - mongodb-driver-server.ishidden.md: '« MongoDB\\Driver\\Server::isHidden'
  - mongodb-driver-server.isprimary.md: 'MongoDB\\Driver\\Server::isPrimary »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::isPassive'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::isPassive

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::isPassive — Перевіряє, чи є сервер пасивним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isPassive(): bool
```

Повертає, чи є цей сервер [»пасивним членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-passive-member)набора реплик (то есть его приоритет равен

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є пасивним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
