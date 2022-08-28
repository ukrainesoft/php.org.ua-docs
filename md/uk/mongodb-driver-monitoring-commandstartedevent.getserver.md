Повертає сервер, на якому було виконано команду

-   [« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId](mongodb-driver-monitoring-commandstartedevent.getrequestid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServerConnectionId »](mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає сервер, на якому було виконано команду
    

# MongoDBDriverMonitoringCommandStartedEvent::getServer

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getServer — Повертає сервер, на якому було виконано команду

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html), на якому було виконано команду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html), на якому було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer()](mongodb-driver-monitoring-commandfailedevent.getserver.html) - Повертає сервер, на якому було виконано команду
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer()](mongodb-driver-monitoring-commandsucceededevent.getserver.html) - Повертає сервер, на якому було виконано команду
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)