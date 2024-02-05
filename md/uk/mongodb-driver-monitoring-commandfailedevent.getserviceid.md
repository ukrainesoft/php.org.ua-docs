---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getserverconnectionid.md: '« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServerConnectionId'
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDB\\Driver\\Monitoring\\CommandStartedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDB\\Driver\\Monitoring\\CommandFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId

(mongodb >=1.11.0)

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId — Повертає ідентифікатор служби балансувальника навантаження для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getServiceId(): ?MongoDB\BSON\ObjectId
```

Якщо драйвер підключено до кластера MongoDB через балансувальник навантаження, ідентифікатор служби відповідає полю `serviceId`в ответе на команду`hello`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор служби балансувальника навантаження або **`null`**, якщо драйвер не підключено до балансувальника навантаження.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
