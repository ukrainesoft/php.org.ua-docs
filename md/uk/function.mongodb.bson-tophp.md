Повертає PHP подання значення BSON

-   [« MongoDBBSONtoJSON](function.mongodb.bson-tojson.html)
    
-   [MongoDBBSONtoRelaxedExtendedJSON »](function.mongodb.bson-torelaxedextendedjson.html)
    
-   [PHP Manual](index.md)
    
-   [Функції](ref.bson.functions.md)
    
-   Повертає PHP подання значення BSON
    

# MongoDBBSONtoPHP

(mongodb >=1.0.0)

MongoDBBSONtoPHP — Повертає PHP уявлення значення BSON

### Опис

```methodsynopsis
MongoDB\BSON\toPHP(string $bson, array $typeMap = array()): array|object
```

Десеріалізує документ BSON (тобто двійковий рядок) у його представлення PHP. Параметр `typeMap` може використовуватися для керування типами PHP, що використовуються для перетворення масивів та документів BSON (як кореневих, так і вбудованих).

**Увага**

Документи BSON технічно можуть містити ключі, що повторюються, оскільки документи зберігаються у вигляді списку пар ключ-значення; однак програмам слід утримуватися від створення документів з дублікатами ключів, оскільки поведінка сервера та драйвера може бути невизначеною. Оскільки об'єкти та масиви PHP не можуть мати ключів, що повторюються, дані також можуть бути втрачені при декодуванні документа BSON з повторюваними ключами.

### Список параметрів

`bson` (string)

Значення BSON для десеріалізації.

`typeMap` (array)

[Конфігурація карти типів](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps)

### Значення, що повертаються

Десеріалізоване значення PHP.

### Помилки

-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо клас у карті типів не може бути створений або не реалізує [MongoDBBSONUnserializable](class.mongodb-bson-unserializable.html)
-   Виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) викидається, якщо вхідні дані не є одним документом BSON. Можливі причини включають, але не обмежені некоректним BSON, зайвими даними або несподіваною помилкою [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson)

### список змін

| Версия                                                                                                                                                                                     | Описание |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| PECL mongodb 1.4.0                                                                                                                                                                         |          |
| Якщо вхідні дані містять непідтримуваний застарілий тип BSON, драйвер більше не буде записувати попередження в журнал налагодження, а натомість створить об'єкт, який представляє цей тип. |          |

| | PECL mongodb 1.3.2 |

[MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) більше не видається, якщо вхідні дані містять непідтримуваний тип BSON. Такі типи будуть ігноруватися (як вони були у версіях до 1.3.0), хоча драйвер тепер записуватиме попередження в журнал налагодження (дивіться: [mongodb.debug](mongodb.configuration.html#ini.mongodb.debug)

| | PECL mongodb 1.3.0

[MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) видається, якщо вхідні дані містять непідтримуваний тип BSON. Раніше такі типи нехтували.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONtoPHP()****

```php
<?php

$bson = hex2bin('0e00000010666f6f000100000000');
$value = MongoDB\BSON\toPHP($bson);
var_dump($value);

?>
```

Результат виконання цього прикладу:

```
object(stdClass)#1 (1) {
  ["foo"]=>
  int(1)
}
```

### Дивіться також

-   [MongoDBBSONfromPHP()](function.mongodb.bson-fromphp.html) - Повертає представлення BSON значення PHP
-   [» MongoDB BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
-   [Постійні дані](mongodb.persistence.md)