Повертає ім'я команди

-   [« MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   [MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros »](mongodb-driver-monitoring-commandfailedevent.getdurationmicros.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   Повертає ім'я команди
    

# MongoDBDriverMonitoringCommandFailedEvent::getCommandName

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getCommandName — Повертає ім'я команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getCommandName(): string
```

Повертає ім'я команди (наприклад, `"find"` `"aggregate"`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)