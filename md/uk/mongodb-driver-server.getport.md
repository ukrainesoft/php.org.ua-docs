---
navigation:
  - mongodb-driver-server.getlatency.md: '« MongoDB\\Driver\\Server::getLatency'
  - mongodb-driver-server.getserverdescription.md: 'MongoDB\\Driver\\Server::getServerDescription »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::getPort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::getPort

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::getPort — Повертає порт, який слухає сервер

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Server::getPort()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getPort());

?>
```

Результат виконання наведеного прикладу:

```
int(27017)
```

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
-   [MongoDB\\Driver\\ServerDescription::getPort()](mongodb-driver-serverdescription.getport.md) \- Повертає порт, на якому прослуховується цей сервер
