---
navigation:
  - mongodb-driver-serverdescription.gettype.md: '« MongoDB\\Driver\\ServerDescription::getType'
  - mongodb-driver-topologydescription.getservers.md: 'MongoDB\\Driver\\TopologyDescription::getServers »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\TopologyDescription
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\TopologyDescription

(mongodb >=1.13.0)

## Вступ

Класс**MongoDB\\Driver\\TopologyDescription** є об'єктом значення, що представляє топологію, до якої підключений драйвер. Примірники класу повертаються методами [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.md)

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\TopologyDescription
     
     {
    
    /* Константы */
    
     const
     string
      TYPE_UNKNOWN = "Unknown";

    const
     string
      TYPE_SINGLE = "Single";

    const
     string
      TYPE_SHARDED = "Sharded";

    const
     string
      TYPE_REPLICA_SET_NO_PRIMARY = "ReplicaSetNoPrimary";

    const
     string
      TYPE_REPLICA_SET_WITH_PRIMARY = "ReplicaSetWithPrimary";

    const
     string
      TYPE_LOAD_BALANCED = "LoadBalanced";


    /* Методы */
    
   final public getServers(): array
final public getType(): string
final public hasReadableServer(?MongoDB\Driver\ReadPreference $readPreference = null): bool
final public hasWritableServer(): bool

   }
```

## Обумовлені константи

**`MongoDB\Driver\TopologyDescription::TYPE_UNKNOWN`**

Невідомий тип топології, який повертається методом [MongoDB\\Driver\\TopologyDescription::getType()](mongodb-driver-topologydescription.gettype.md)

**`MongoDB\Driver\TopologyDescription::TYPE_SINGLE`**

Одиночний сервер (тобто пряме з'єднання), що повертається методом [MongoDB\\Driver\\TopologyDescription::getType()](mongodb-driver-topologydescription.gettype.md)

**`MongoDB\Driver\TopologyDescription::TYPE_SHARDED`**

Кластер, що розділяється, повертається методом [MongoDB\\Driver\\TopologyDescription::getType()](mongodb-driver-topologydescription.gettype.md)

**`MongoDB\Driver\TopologyDescription::TYPE_REPLICA_SET_NO_PRIMARY`**

Набір реплік без первинного сервера, який повертається методом [MongoDB\\Driver\\TopologyDescription::getType()](mongodb-driver-topologydescription.gettype.md)

**`MongoDB\Driver\TopologyDescription::TYPE_REPLICA_SET_WITH_PRIMARY`**

Набір реплік з первинним сервером, який повертається методом [MongoDB\\Driver\\TopologyDescription::getType()](mongodb-driver-topologydescription.gettype.md)

**`MongoDB\Driver\TopologyDescription::TYPE_LOAD_BALANCED`**

Збалансована за навантаженням топологія, що повертається методом [MongoDB\\Driver\\TopologyDescription::getType()](mongodb-driver-topologydescription.gettype.md)

## Зміст

-   [MongoDB\\Driver\\TopologyDescription::getServers](mongodb-driver-topologydescription.getservers.md)— Повертає сервери у топології
-   [MongoDB\\Driver\\TopologyDescription::getType](mongodb-driver-topologydescription.gettype.md)— Повертає рядок, що позначає тип топології
-   [MongoDB\\Driver\\TopologyDescription::hasReadableServer](mongodb-driver-topologydescription.hasreadableserver.md)— Повертає, чи є у топології сервер, доступний для читання
-   [MongoDB\\Driver\\TopologyDescription::hasWritableServer](mongodb-driver-topologydescription.haswritableserver.md)— Повертає, чи є у топології сервер, доступний для запису
