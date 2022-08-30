Повертає ідентифікатор служби балансувальника навантаження для команди

-   [« MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId](mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent »](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає ідентифікатор служби балансувальника навантаження для команди
    

# MongoDBDriverMonitoringCommandStartedEvent::getServiceId

(mongodb >=1.11.0)

MongoDBDriverMonitoringCommandStartedEvent::getServiceId — Повертає ідентифікатор служби балансувальника навантаження для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getServiceId(): ?MongoDB\BSON\ObjectId
```

Якщо драйвер підключено до кластера MongoDB через балансувальник навантаження, ідентифікатор служби відповідає полю `serviceId` у відповіді на команду `hello`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор служби балансувальника навантаження або **`null`**, якщо драйвер не підключено до балансувальника навантаження.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)