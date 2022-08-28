Повертає останню відповідь сервера "hello"

-   [« MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.html)
    
-   [MongoDB\\Driver\\ServerDescription::getHost »](mongodb-driver-serverdescription.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.html)
    
-   Повертає останню відповідь сервера "hello"
    

# MongoDBDriverServerDescription::getHelloResponse

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getHelloResponse — Повертає останню відповідь сервера "hello"

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getHelloResponse(): array
```

Повертає масив інформації, що описує сервер. Цей масив формується з останнього (на момент створення [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.html)) відповіді команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) відповідь команди, отримана за допомогою [» мониторинга сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

> **Зауваження**
> 
> Якщо драйвер підключено до балансувальника навантаження, метод поверне порожній масив, оскільки балансувальники навантаження не відстежуються. На відміну від [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.html), яка повертає відповідь команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) від початкового рукостискання з'єднання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив інформації, що описує сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер
-   Команда [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/) у посібнику з MongoDB
-   [» Спецификация обнаружения и мониторинга серверов](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)