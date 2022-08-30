Повертає ім'я команди

-   [« MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros »](mongodb-driver-monitoring-commandsucceededevent.getdurationmicros.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає ім'я команди
    

# MongoDBDriverMonitoringCommandSucceededEvent::getCommandName

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getCommandName — Повертає ім'я команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getCommandName(): string
```

Повертає ім'я команди (наприклад, `"find"` `"aggregate"`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)