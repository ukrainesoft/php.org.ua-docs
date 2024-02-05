---
navigation:
  - class.mongodb-driver-serverdescription.md: « MongoDB\\Driver\\ServerDescription
  - mongodb-driver-serverdescription.gethost.md: 'MongoDB\\Driver\\ServerDescription::getHost »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.md: MongoDB\\Driver\\ServerDescription
title: 'MongoDB\\Driver\\ServerDescription::getHelloResponse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerDescription::getHelloResponse

(mongodb >=1.13.0)

MongoDB\\Driver\\ServerDescription::getHelloResponse — Повертає останню відповідь сервера "hello"

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getHelloResponse(): array
```

Повертає масив інформації, що описує сервер. Цей масив формується з останнього (на момент створення [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.md)) відповіді команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) відповідь команди, отримана за допомогою [» моніторингу сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

> **Зауваження** :
> 
> Якщо драйвер підключено до балансувальника навантаження, метод поверне порожній масив, оскільки балансувальники навантаження не відстежуються. На відміну від [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md), яка повертає відповідь команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) від початкового рукостискання з'єднання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив інформації, що описує сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
-   Команда[» hello](https://www.mongodb.com/docs/manual/reference/command/hello/)у посібнику з MongoDB
-   [» Специфікація виявлення та моніторингу серверів](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)
