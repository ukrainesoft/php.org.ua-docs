---
navigation:
  - mongodb-driver-server.executewritecommand.html: '« MongoDBDriverServer::executeWriteCommand'
  - mongodb-driver-server.getinfo.html: 'MongoDBDriverServer::getInfo »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.html: MongoDBDriverServer
title: 'MongoDBDriverServer::getHost'
---
# MongoDBDriverServer::getHost

(mongodb >=1.0.0)

MongoDBDriverServer::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getHost(): string
```

Повертає ім'я сервера хоста.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverServer::getHost()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getHost());

?>
```

Результат виконання цього прикладу:

```
string(9) "localhost"
```

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер
-   [MongoDBDriverServerDescription::getHost()](mongodb-driver-serverdescription.gethost.html) - Повертає ім'я сервера хоста
