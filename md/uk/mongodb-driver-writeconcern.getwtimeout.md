---
navigation:
  - mongodb-driver-writeconcern.getw.md: '« MongoDB\\Driver\\WriteConcern::getW'
  - mongodb-driver-writeconcern.isdefault.md: 'MongoDB\\Driver\\WriteConcern::isDefault »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDB\\Driver\\WriteConcern
title: 'MongoDB\\Driver\\WriteConcern::getWtimeout'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcern::getWtimeout

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteConcern::getWtimeout — Повертає опцію "wtimeout" WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::getWtimeout(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "wtimeout" WriteConcern.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.7.0 | У 32-розрядних системах метод завжди буде усікати значення `wTimeout`якщо воно виходить за межі 32-бітного діапазону. У цьому випадку буде видано попередження. |

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\WriteConcern::getWtimeout()\*\*\*\*

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getWtimeout());

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 3000);
var_dump($wc->getWtimeout());

?>
```

Результат виконання наведеного прикладу:

```
int(0)
int(3000)
```

### Дивіться також

-   [» Посібник з гарантії запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
