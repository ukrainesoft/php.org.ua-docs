Повертає ім'я сервера хоста

-   [« MongoDBDriverMonitoringServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
    
-   [MongoDBDriverMonitoringServerChangedEvent::getNewDescription »](mongodb-driver-monitoring-serverchangedevent.getnewdescription.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
    
-   Повертає ім'я сервера хоста
    

# MongoDBDriverMonitoringServerChangedEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)