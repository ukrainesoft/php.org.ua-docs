Повертає сервер, на якому було виконано команду

-   [« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId »](mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає сервер, на якому було виконано команду
    

# MongoDBDriverMonitoringCommandSucceededEvent::getServer

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getServer — Повертає сервер, на якому було виконано команду

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getServer(): MongoDB\Driver\Server
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
-   [MongoDB\\Driver\\Cursor::getServer()](mongodb-driver-cursor.getserver.html) - Повертає сервер, пов'язаний із курсором
-   [MongoDB\\Driver\\WriteResult::getServer()](mongodb-driver-writeresult.getserver.html) - Повертає сервер, пов'язаний із цим результатом запису
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)