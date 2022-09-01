---
navigation:
  - class.mongodb-driver-serverdescription.html: « MongoDBDriverServerDescription
  - mongodb-driver-serverdescription.gethost.html: 'MongoDBDriverServerDescription::getHost »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.html: MongoDBDriverServerDescription
title: 'MongoDBDriverServerDescription::getHelloResponse'
---
# MongoDBDriverServerDescription::getHelloResponse

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getHelloResponse — Повертає останню відповідь сервера "hello"

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getHelloResponse(): array
```

Повертає масив інформації, що описує сервер. Цей масив формується з останнього (на момент створення [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.md)) відповіді команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) відповідь команди, отримана за допомогою [» мониторинга сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

> **Зауваження**
> 
> Якщо драйвер підключено до балансувальника навантаження, метод поверне порожній масив, оскільки балансувальники навантаження не відстежуються. На відміну від [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.md), яка повертає відповідь команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) від початкового рукостискання з'єднання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив інформації, що описує сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.md) - Повертає масив інформації, що описує сервер
-   Команда [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) у посібнику з MongoDB
-   [» Спецификация обнаружения и мониторинга серверов](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)
