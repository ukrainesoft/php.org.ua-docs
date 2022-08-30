Повертає сервер, на якому було виконано команду

-   [« MongoDBDriverMonitoringCommandStartedEvent::getRequestId](mongodb-driver-monitoring-commandstartedevent.getrequestid.html)
    
-   [MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId »](mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає сервер, на якому було виконано команду
    

# MongoDBDriverMonitoringCommandStartedEvent::getServer

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getServer — Повертає сервер, на якому було виконано команду

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html), на якому було виконано команду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html), на якому було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandFailedEvent::getServer()](mongodb-driver-monitoring-commandfailedevent.getserver.html) - Повертає сервер, на якому було виконано команду
-   [MongoDBDriverMonitoringCommandSucceededEvent::getServer()](mongodb-driver-monitoring-commandsucceededevent.getserver.html) - Повертає сервер, на якому було виконано команду
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)