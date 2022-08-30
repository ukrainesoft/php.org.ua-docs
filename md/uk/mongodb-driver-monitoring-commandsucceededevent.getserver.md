Повертає сервер, на якому було виконано команду

-   [« MongoDBDriverMonitoringCommandSucceededEvent::getRequestId](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent::getServerConnectionId »](mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає сервер, на якому було виконано команду
    

# MongoDBDriverMonitoringCommandSucceededEvent::getServer

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getServer — Повертає сервер, на якому було виконано команду

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html), на якому було виконано команду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html), на якому було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getServer()](mongodb-driver-monitoring-commandstartedevent.getserver.html) - Повертає сервер, на якому було виконано команду
-   [MongoDBDriverCursor::getServer()](mongodb-driver-cursor.getserver.html) - Повертає сервер, пов'язаний із курсором
-   [MongoDBDriverWriteResult::getServer()](mongodb-driver-writeresult.getserver.html) - Повертає сервер, пов'язаний із цим результатом запису
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)