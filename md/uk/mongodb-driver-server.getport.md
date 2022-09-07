---
navigation:
  - mongodb-driver-server.getlatency.md: '« MongoDBDriverServer::getLatency'
  - mongodb-driver-server.getserverdescription.md: 'MongoDBDriverServer::getServerDescription »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::getPort'
---
# MongoDBDriverServer::getPort

(mongodb >=1.0.0)

MongoDBDriverServer::getPort — Повертає порт, який слухає сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getPort(): int
```

Повертає порт, який слухає сервер.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, який слухає сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverServer::getPort()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getPort());

?>
```

Результат виконання цього прикладу:

```
int(27017)
```

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.md) - Повертає масив інформації, що описує сервер
-   [MongoDBDriverServerDescription::getPort()](mongodb-driver-serverdescription.getport.md) - Повертає порт, на якому прослуховується цей сервер
