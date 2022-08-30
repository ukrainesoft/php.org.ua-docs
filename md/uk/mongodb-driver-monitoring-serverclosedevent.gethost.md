Повертає ім'я сервера хоста

-   [« MongoDBDriverMonitoringServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html)
    
-   [MongoDBDriverMonitoringServerClosedEvent::getPort »](mongodb-driver-monitoring-serverclosedevent.getport.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html)
    
-   Повертає ім'я сервера хоста
    

# MongoDBDriverMonitoringServerClosedEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerClosedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)