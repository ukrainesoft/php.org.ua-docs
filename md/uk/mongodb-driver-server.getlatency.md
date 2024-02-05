---
navigation:
  - mongodb-driver-server.getinfo.md: '« MongoDB\\Driver\\Server::getInfo'
  - mongodb-driver-server.getport.md: 'MongoDB\\Driver\\Server::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::getLatency'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::getLatency

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::getLatency — Повертає затримку сервера в мілісекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getLatency(): ?integer
```

Повертає затримку сервера у мілісекундах. Виміряне клієнтом [» час проходження](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst#round-trip-time) команди `hello`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає затримку сервера в мілісекундах або **`null`**, якщо затримка не була виміряна (наприклад, клієнт підключений до балансувальника навантаження).

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.11.0 | Метод поверне \*\*`null`\*\*якщо затримка не була виміряна. У попередніх версіях завжди поверталося ціле число, а невстановлене значення могло відображатися як `-1` |

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Server::getLatency()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getLatency());

?>
```

Висновок наведеного прикладу буде схожим на:

```
int(592)
```

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
-   [MongoDB\\Driver\\ServerDescription::getRoundTripTime()](mongodb-driver-serverdescription.getroundtriptime.md) \- Повертає час обходу сервера у мілісекундах
-   [» Специфікація виявлення та моніторингу сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)
