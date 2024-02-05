---
navigation:
  - mongodb-driver-server.isprimary.md: '« MongoDB\\Driver\\Server::isPrimary'
  - class.mongodb-driver-serverdescription.md: MongoDB\\Driver\\ServerDescription »
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::isSecondary'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::isSecondary

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::isSecondary — Перевіряє, чи є сервер другорядним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isSecondary(): bool
```

Повертає, чи є цей сервер [» другорядним членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-secondary)набора реплик.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є другорядним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
