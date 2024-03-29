---
navigation:
  - mongodb-driver-clientencryption.rewrapmanydatakey.md: '« MongoDB\\Driver\\ClientEncryption::rewrapManyDataKey'
  - mongodb-driver-serverapi.bsonserialize.md: 'MongoDB\\Driver\\ServerApi::bsonSerialize »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\ServerApi
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\ServerApi

(mongodb >=1.10.0)

## Вступ

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\ServerApi
     
     implements 
       MongoDB\BSON\Serializable,  Serializable {

    /* Константы */
    
     const
     string
      MongoDB\Driver\ServerAPI::V1 = "1";


    /* Методы */
    
   final public bsonSerialize(): stdClass
final public __construct(string $version, ?bool $strict = null, ?bool $deprecationErrors = null)
final public serialize(): string
final public unserialize(string $data): void

   }
```

## Обумовлені константи

**`MongoDB\Driver\ServerApi::V1`**

Server API Версія 1.

## Приклади

**Приклад #1 Приклад оголошення версії API у диспетчері**

```php
<?php

use MongoDB\Driver\Manager;
use MongoDB\Driver\ServerApi;

$v1 = new ServerApi(ServerApi::v1);
$manager = new Manager('mongodb://localhost:27017', [], ['serverApi' => $v1]);

$command = new MongoDB\Driver\Command(['buildInfo' => 1]);

try {
    $cursor = $manager->executeCommand('admin', $command);
} catch(MongoDB\Driver\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}

/* Команда buildInfo возвращает единственный документ результата, поэтому нам нужно получить доступ
 * к первому результату в курсоре. */
$buildInfo = $cursor->toArray()[0];

echo $buildInfo->version, "\n";

?>
```

Результат виконання наведеного прикладу:

```
4.9.0-alpha7-49-gb968ca0
```

**Приклад #2 Приклад оголошення строгої версії API для менеджера**

У наступному прикладі встановлюється прапор `strict`, який повідомляє серверу відхилити будь-яку команду, яка не є частиною оголошеної версії API. Це призводить до помилки під час виконання команди buildInfo.

```php
<?php

use MongoDB\Driver\Manager;
use MongoDB\Driver\ServerApi;

$v1 = new ServerApi(ServerApi::v1, true);
$manager = new Manager('mongodb://localhost:27017', [], ['serverApi' => $v1]);

$command = new MongoDB\Driver\Command(['buildInfo' => 1]);

try {
    $cursor = $manager->executeCommand('admin', $command);
} catch(MongoDB\Driver\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}

/* Команда buildInfo возвращает единственный документ результата, поэтому нам нужно получить доступ
 * к первому результату в курсоре. */
$buildInfo = $cursor->toArray()[0];

echo $buildInfo->version, "\n";

?>
```

Результат виконання наведеного прикладу:

```
Provided apiStrict:true, but the command buildInfo is not in API Version 1
```

## Зміст

-   [MongoDB\\Driver\\ServerApi::bsonSerialize](mongodb-driver-serverapi.bsonserialize.md)— Повертає об'єкт для серіалізації BSON
-   [MongoDB\\Driver\\ServerApi::\_\_construct](mongodb-driver-serverapi.construct.md)— Створює новий примірник ServerApi
-   [MongoDB\\Driver\\ServerApi::serialize](mongodb-driver-serverapi.serialize.md) \- Серіалізує ServerApi
-   [MongoDB\\Driver\\ServerApi::unserialize](mongodb-driver-serverapi.unserialize.md) \- Десеріалізує ServerApi
