Повертає ідентифікатор служби балансувальника навантаження для команди

-   [« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId](mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent »](class.mongodb-driver-monitoring-serverchangedevent.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає ідентифікатор служби балансувальника навантаження для команди
    

# MongoDBDriverMonitoringCommandSucceededEvent::getServiceId

(mongodb >=1.11.0)

MongoDBDriverMonitoringCommandSucceededEvent::getServiceId — Повертає ідентифікатор служби балансувальника навантаження для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getServiceId(): ?MongoDB\BSON\ObjectId
```

Якщо драйвер підключено до кластера MongoDB через балансувальник навантаження, ідентифікатор служби відповідає полю `serviceId` у відповіді на команду `hello`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор служби балансувальника навантаження або **`null`**, якщо драйвер не підключено до балансувальника навантаження.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)