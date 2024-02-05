---
navigation:
  - mongodb-driver-server.executewritecommand.md: '« MongoDB\\Driver\\Server::executeWriteCommand'
  - mongodb-driver-server.getinfo.md: 'MongoDB\\Driver\\Server::getInfo »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::getHost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::getHost

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::getHost — Повертає ім'я сервера.

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\Server::getHost()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getHost());

?>
```

Результат виконання наведеного прикладу:

```
string(9) "localhost"
```

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
-   [MongoDB\\Driver\\ServerDescription::getHost()](mongodb-driver-serverdescription.gethost.md) \- Повертає ім'я сервера хоста
