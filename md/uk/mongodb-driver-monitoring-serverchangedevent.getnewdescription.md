Повертає новий опис сервера

-   [« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost](mongodb-driver-monitoring-serverchangedevent.gethost.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort »](mongodb-driver-monitoring-serverchangedevent.getport.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
    
-   Повертає новий опис сервера
    

# MongoDBDriverMonitoringServerChangedEvent::getNewDescription

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getNewDescription — Повертає новий опис сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getNewDescription(): MongoDB\Driver\ServerDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий опис ([MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.html)) сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)