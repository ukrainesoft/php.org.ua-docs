Повертає ідентифікатор з'єднання із сервером для команди

-   [« MongoDBDriverMonitoringCommandStartedEvent::getServer](mongodb-driver-monitoring-commandstartedevent.getserver.html)
    
-   [MongoDBDriverMonitoringCommandStartedEvent::getServiceId »](mongodb-driver-monitoring-commandstartedevent.getserviceid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає ідентифікатор з'єднання із сервером для команди
    

# MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId

(mongodb >=1.14.0)

MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId — Повертає ідентифікатор з'єднання із сервером для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getServerConnectionId(): ?int
```

Повертає ідентифікатор з'єднання із сервером для команди. Ідентифікатор з'єднання з сервером відрізняється від сервера (тобто . [MongoDBDriverMonitoringCommandStartedEvent::getServer()](mongodb-driver-monitoring-commandstartedevent.getserver.html)) і повертається у поле "connectionId" з відповіді команди `hello` у MongoDB 4.2+.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор з'єднання із сервером або \*\*`null`\*\*якщо він недоступний.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)