---
navigation:
  - mongodb-driver-server.gethost.md: '« MongoDB\\Driver\\Server::getHost'
  - mongodb-driver-server.getlatency.md: 'MongoDB\\Driver\\Server::getLatency »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::getInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::getInfo

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::getInfo — Повертає масив інформації, що описує сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getInfo(): array
```

Повертає масив інформації, що описує сервер. Цей масив отримано з останньої відповіді команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/), полученного с помощью[» моніторингу сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

> **Зауваження** :
> 
> Коли драйвер підключено до балансувальника навантаження, метод поверне відповідь на команду [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) від резервного сервера під час початкового підтвердження з'єднання. Це відрізняється від інших методів (наприклад, [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.md)), які повертають інформацію про самого балансувальника навантаження.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив інформації, що описує сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Server::getInfo()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/');

$rp = new MongoDB\Driver\ReadPreference('primary');
$server = $manager->selectServer($rp);

var_dump($server->getInfo());

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(23) {
  ["helloOk"]=>
  bool(true)
  ["topologyVersion"]=>
  array(2) {
    ["processId"]=>
    object(MongoDB\BSON\ObjectId)#4 (1) {
      ["oid"]=>
      string(24) "617b6d696a3a89d2f77e6df0"
    }
    ["counter"]=>
    int(6)
  }
  ["hosts"]=>
  array(1) {
    [0]=>
    string(15) "localhost:27017"
  }
  ["setName"]=>
  string(3) "rs0"
  ["setVersion"]=>
  int(1)
  ["ismaster"]=>
  bool(true)
  ["secondary"]=>
  bool(false)
  ["primary"]=>
  string(15) "localhost:27017"
  ["me"]=>
  string(15) "localhost:27017"
  ["electionId"]=>
  object(MongoDB\BSON\ObjectId)#5 (1) {
    ["oid"]=>
    string(24) "7fffffff0000000000000001"
  }
  ["lastWrite"]=>
  array(4) {
    ["opTime"]=>
    array(2) {
      ["ts"]=>
      object(MongoDB\BSON\Timestamp)#6 (2) {
        ["increment"]=>
        string(1) "1"
        ["timestamp"]=>
        string(10) "1635478989"
      }
      ["t"]=>
      int(1)
    }
    ["lastWriteDate"]=>
    object(MongoDB\BSON\UTCDateTime)#7 (1) {
      ["milliseconds"]=>
      string(13) "1635478989000"
    }
    ["majorityOpTime"]=>
    array(2) {
      ["ts"]=>
      object(MongoDB\BSON\Timestamp)#8 (2) {
        ["increment"]=>
        string(1) "1"
        ["timestamp"]=>
        string(10) "1635478989"
      }
      ["t"]=>
      int(1)
    }
    ["majorityWriteDate"]=>
    object(MongoDB\BSON\UTCDateTime)#9 (1) {
      ["milliseconds"]=>
      string(13) "1635478989000"
    }
  }
  ["maxBsonObjectSize"]=>
  int(16777216)
  ["maxMessageSizeBytes"]=>
  int(48000000)
  ["maxWriteBatchSize"]=>
  int(100000)
  ["localTime"]=>
  object(MongoDB\BSON\UTCDateTime)#10 (1) {
    ["milliseconds"]=>
    string(13) "1635478992136"
  }
  ["logicalSessionTimeoutMinutes"]=>
  int(30)
  ["connectionId"]=>
  int(3)
  ["minWireVersion"]=>
  int(0)
  ["maxWireVersion"]=>
  int(13)
  ["readOnly"]=>
  bool(false)
  ["ok"]=>
  float(1)
  ["$clusterTime"]=>
  array(2) {
    ["clusterTime"]=>
    object(MongoDB\BSON\Timestamp)#11 (2) {
      ["increment"]=>
      string(1) "1"
      ["timestamp"]=>
      string(10) "1635478989"
    }
    ["signature"]=>
    array(2) {
      ["hash"]=>
      object(MongoDB\BSON\Binary)#12 (2) {
        ["data"]=>
        string(20) ""
        ["type"]=>
        int(0)
      }
      ["keyId"]=>
      int(0)
    }
  }
  ["operationTime"]=>
  object(MongoDB\BSON\Timestamp)#13 (2) {
    ["increment"]=>
    string(1) "1"
    ["timestamp"]=>
    string(10) "1635478989"
  }
}
```

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.11.0 | Коли драйвер підключено до системи балансування навантаження, метод повертає відповідь на команду. `hello` допоміжного сервера під час початкового підтвердження з'єднання. |

### Дивіться також

-   [MongoDB\\Driver\\ServerDescription::getHelloResponse()](mongodb-driver-serverdescription.gethelloresponse.md) - Повертає останню відповідь сервера "hello"
-   Команда[» hello](https://www.mongodb.com/docs/manual/reference/command/hello/)у посібнику MongoDB
-   [» Посібник з виявлення та моніторингу серверів](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)
