Повертає ідентифікатор з'єднання із сервером для команди

-   [« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer](mongodb-driver-monitoring-commandstartedevent.getserver.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServiceId »](mongodb-driver-monitoring-commandstartedevent.getserviceid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає ідентифікатор з'єднання із сервером для команди
    

# MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId

(mongodb >=1.14.0)

MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId — Повертає ідентифікатор з'єднання із сервером для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getServerConnectionId(): ?int
```

Повертає ідентифікатор з'єднання із сервером для команди. Ідентифікатор з'єднання з сервером відрізняється від сервера (тобто . [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer()](mongodb-driver-monitoring-commandstartedevent.getserver.html)) і повертається у поле "connectionId" з відповіді команди `hello` у MongoDB 4.2+.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор з'єднання із сервером або **`null`**якщо він недоступний.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)