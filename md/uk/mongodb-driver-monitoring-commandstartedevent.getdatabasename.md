Повертає базу даних, на якій виконувалась команда

-   [« MongoDBDriverMonitoringCommandStartedEvent::getCommandName](mongodb-driver-monitoring-commandstartedevent.getcommandname.html)
    
-   [MongoDBDriverMonitoringCommandStartedEvent::getOperationId »](mongodb-driver-monitoring-commandstartedevent.getoperationid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає базу даних, на якій виконувалась команда
    

# MongoDBDriverMonitoringCommandStartedEvent::getDatabaseName

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getDatabaseName — Повертає базу даних, на якій виконувалась команда

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getDatabaseName(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає базу даних, на якій було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)