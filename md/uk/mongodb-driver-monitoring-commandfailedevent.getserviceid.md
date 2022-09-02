---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getserverconnectionid.md: '« MongoDBDriverMonitoringCommandFailedEvent::getServerConnectionId'
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDBDriverMonitoringCommandStartedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDBDriverMonitoringCommandFailedEvent
title: 'MongoDBDriverMonitoringCommandFailedEvent::getServiceId'
---
# MongoDBDriverMonitoringCommandFailedEvent::getServiceId

(mongodb >=1.11.0)

MongoDBDriverMonitoringCommandFailedEvent::getServiceId — Повертає ідентифікатор служби балансувальника навантаження для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getServiceId(): ?MongoDB\BSON\ObjectId
```

Якщо драйвер підключено до кластера MongoDB через балансувальник навантаження, ідентифікатор служби відповідає полю `serviceId` у відповіді на команду `hello`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор служби балансувальника навантаження або **`null`**, якщо драйвер не підключено до балансувальника навантаження.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
