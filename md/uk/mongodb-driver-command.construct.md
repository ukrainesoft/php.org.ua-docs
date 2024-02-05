---
navigation:
  - class.mongodb-driver-command.md: « MongoDB\\Driver\\Command
  - class.mongodb-driver-query.md: MongoDB\\Driver\\Query »
  - index.md: PHP Manual
  - class.mongodb-driver-command.md: MongoDB\\Driver\\Command
title: 'MongoDB\\Driver\\Command::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Command::\_\_construct

(mongodb >=1.0.0)

MongoDB\\Driver\\Command::\_\_construct — Створює новий об'єкт Command

### Опис

```methodsynopsis
final public MongoDB\Driver\Command::__construct(array|object $document, ?array $commandOptions = null)
```

Створює новий об'єкт класу [MongoDB\\Driver\\Command](class.mongodb-driver-command.md)що є незмінним значенням, що представляє команду бази даних. Цю команду згодом можна запустити за допомогою [MongoDB\\Driver\\Manager::executeCommand()](mongodb-driver-manager.executecommand.md)

Повний документ команди, що включає її ім'я та інші опції, має бути заданий у параметрі `document`Параметр`commandOptions` використовується тільки для визначення опцій запуску команди та результуючий [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)

### Список параметрів

`document`

Повний документ команди, який буде передано серверу.

`commandOptions`

> **Зауваження**: Не використовуйте цей параметр, щоб вказати опції, описані в посібнику з команд MongoDB. Цей параметр можна використовувати лише для наведених нижче опцій.

**commandOptions**

| Опция | Тип | Опис |
| --- | --- | --- |
| maxAwaitTimeMS | int |  |
| Позитивне ціле число, яке визначає обмеження часу в мілісекундах, на яке сервер може блокувати операцію getMore, якщо дані відсутні. Ця опція може використовуватися лише спільно з командами, що повертають хвостові курсори. (наприклад [» Change Streams](https://www.mongodb.com/docs/manual/changeStreams/) |  |  |

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.4.0 |  |
| Доданий другий аргумент `commandOptions`, що дозволяє визначити опцію `"maxAwaitTimeMS"` |  |

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Command::\_\_construct()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$command = new MongoDB\Driver\Command(array("buildinfo" => 1));

try {
    $cursor = $manager->executeCommand("admin", $command);
    $response = $cursor->toArray()[0];
} catch(MongoDB\Driver\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}
var_dump($response);

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(13) {
  ["version"]=>
  string(14) "2.8.0-rc2-pre-"
  ["gitVersion"]=>
  string(62) "b743d7158f7642f4da6b7eac8320374b3b88dc2e modules: subscription"
  ["OpenSSLVersion"]=>
  string(25) "OpenSSL 1.0.1f 6 Jan 2014"
  ["sysInfo"]=>
  string(104) "Linux infant 3.16.0-24-generic #32-Ubuntu SMP Tue Oct 28 13:07:32 UTC 2014 x86_64 BOOST_LIB_VERSION=1_49"
  ["loaderFlags"]=>
  string(91) "-fPIC -pthread -Wl,-z,now -rdynamic -Wl,-Bsymbolic-functions -Wl,-z,relro -Wl,-z,now -Wl,-E"
  ["compilerFlags"]=>
  string(301) "-Wnon-virtual-dtor -Woverloaded-virtual -std=c++11 -fPIC -fno-strict-aliasing -ggdb -pthread -Wall -Wsign-compare -Wno-unknown-pragmas -Winvalid-pch -pipe -Werror -O3 -Wno-unused-local-typedefs -Wno-unused-function -Wno-deprecated-declarations -Wno-unused-but-set-variable -fno-builtin-memcmp -std=c99"
  ["allocator"]=>
  string(8) "tcmalloc"
  ["versionArray"]=>
  array(4) {
    [0]=>
    int(2)
    [1]=>
    int(8)
    [2]=>
    int(0)
    [3]=>
    int(-8)
  }
  ["javascriptEngine"]=>
  string(2) "V8"
  ["bits"]=>
  int(64)
  ["debug"]=>
  bool(false)
  ["maxBsonObjectSize"]=>
  int(16777216)
  ["ok"]=>
  float(1)
}
```

**Приклад #2 Приклад використання** MongoDB\\Driver\\Command::\_\_construct()\*\*\*\*

Команди також можуть приймати опції, як частина нормальної структури, яку ви створюєте та відправляєте на сервер. Наприклад, з більшістю команд можна передавати опцію `maxTimeMS` для обмеження часу виконання.

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$command = new MongoDB\Driver\Command(
    array(
        "distinct" => "beer",
        "key" => "beer_name",
        "maxTimeMS" => 10,
    )
);

try {
    $cursor = $manager->executeCommand("beerdb", $command);
    $response = $cursor->toArray()[0];
} catch(MongoDB\Driver\Exception\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}
var_dump($response);

?>
```

Висновок наведеного прикладу буде схожим на:

operation exceeded time limit

### Дивіться також

-   [MongoDB\\Driver\\Manager::executeCommand()](mongodb-driver-manager.executecommand.md) \- Виконує команду бази даних
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)
