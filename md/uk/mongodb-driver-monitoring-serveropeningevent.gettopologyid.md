Returns the topology ID associated with this server

-   [« MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort](mongodb-driver-monitoring-serveropeningevent.getport.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent »](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.html)
    
-   Returns the topology ID associated with this server
    

# MongoDBDriverMonitoringServerOpeningEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerOpeningEvent::getTopologyId — Returns the topology ID associated with this server

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Відображення топології ID.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)