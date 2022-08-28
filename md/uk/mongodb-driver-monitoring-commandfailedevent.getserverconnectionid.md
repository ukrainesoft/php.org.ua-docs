Повертає ідентифікатор з'єднання із сервером для команди

-   [« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer](mongodb-driver-monitoring-commandfailedevent.getserver.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId »](mongodb-driver-monitoring-commandfailedevent.getserviceid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   Повертає ідентифікатор з'єднання із сервером для команди
    

# MongoDBDriverMonitoringCommandFailedEvent::getServerConnectionId

(mongodb >=1.14.0)

MongoDBDriverMonitoringCommandFailedEvent::getServerConnectionId — Повертає ідентифікатор з'єднання з сервером для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getServerConnectionId(): ?int
```

Повертає ідентифікатор з'єднання із сервером для команди. Ідентифікатор підключення до сервера відрізняється від сервера (тобто . [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer()](mongodb-driver-monitoring-commandfailedevent.getserver.html)) і повертається в поле "connectionId" відповіді команди `hello` у MongoDB 4.2+.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор з'єднання із сервером або **`null`**якщо він недоступний.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)