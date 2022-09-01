---
navigation:
  - mongodb-driver-server.getinfo.html: '« MongoDBDriverServer::getInfo'
  - mongodb-driver-server.getport.html: 'MongoDBDriverServer::getPort »'
  - index.html: PHP Manual
  - class.mongodb-driver-server.html: MongoDBDriverServer
title: 'MongoDBDriverServer::getLatency'
---
# MongoDBDriverServer::getLatency

(mongodb >=1.0.0)

MongoDBDriverServer::getLatency — Повертає затримку сервера в мілісекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getLatency(): ?integer
```

Повертає затримку сервера у мілісекундах. Виміряне клієнтом [» время прохождения](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst#round-trip-time) команди `hello`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає затримку сервера в мілісекундах або **`null`**, якщо затримка не була виміряна (наприклад, клієнт підключено до балансувальника навантаження).

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.11.0 | Метод поверне \*\*`null`\*\*якщо затримка не була виміряна. У попередніх версіях завжди поверталося ціле число, а невстановлене значення могло відображатися як `-1` |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverServer::getLatency()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getLatency());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(592)
```

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер
-   [MongoDBDriverServerDescription::getRoundTripTime()](mongodb-driver-serverdescription.getroundtriptime.html) - Повертає час обходу сервера у мілісекундах
-   [» Спецификация обнаружения и мониторинга сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)
