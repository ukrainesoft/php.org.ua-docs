Повертає попередній опис сервера

-   [« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort](mongodb-driver-monitoring-serverchangedevent.getport.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId »](mongodb-driver-monitoring-serverchangedevent.gettopologyid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
    
-   Повертає попередній опис сервера
    

# MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription — Повертає попередній опис сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getPreviousDescription(): MongoDB\Driver\ServerDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній опис ([MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.html)) сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)