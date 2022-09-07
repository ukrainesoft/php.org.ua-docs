---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.md: '« MongoDBDriverMonitoringCommandSucceededEvent::getServerConnectionId'
  - class.mongodb-driver-monitoring-serverchangedevent.md: MongoDBDriverMonitoringServerChangedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.md: MongoDBDriverMonitoringCommandSucceededEvent
title: 'MongoDBDriverMonitoringCommandSucceededEvent::getServiceId'
---
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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
