Повертає сервер, на якому було виконано команду

-   [« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId](mongodb-driver-monitoring-commandfailedevent.getrequestid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServerConnectionId »](mongodb-driver-monitoring-commandfailedevent.getserverconnectionid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   Повертає сервер, на якому було виконано команду
    

# MongoDBDriverMonitoringCommandFailedEvent::getServer

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getServer — Повертає сервер, на якому було виконано команду

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html), на якому було виконано команду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html), на якому було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer()](mongodb-driver-monitoring-commandstartedevent.getserver.html) - Повертає сервер, на якому було виконано команду
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)