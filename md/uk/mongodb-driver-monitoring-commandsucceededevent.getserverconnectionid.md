Повертає ідентифікатор з'єднання із сервером для команди

-   [« MongoDBDriverMonitoringCommandSucceededEvent::getServer](mongodb-driver-monitoring-commandsucceededevent.getserver.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent::getServiceId »](mongodb-driver-monitoring-commandsucceededevent.getserviceid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає ідентифікатор з'єднання із сервером для команди
    

# MongoDBDriverMonitoringCommandSucceededEvent::getServerConnectionId

(mongodb >=1.14.0)

MongoDBDriverMonitoringCommandSucceededEvent::getServerConnectionId — Повертає ідентифікатор з'єднання з сервером для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getServerConnectionId(): ?int
```

Повертає ідентифікатор з'єднання із сервером для команди. Ідентифікатор з'єднання з сервером відрізняється від сервера (тобто . [MongoDBDriverMonitoringCommandSucceededEvent::getServer()](mongodb-driver-monitoring-commandsucceededevent.getserver.html)) і повертається у поле "connectionId" з відповіді команди `hello` у MongoDB 4.2+.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор з'єднання із сервером або \*\*`null`\*\*якщо він недоступний.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)