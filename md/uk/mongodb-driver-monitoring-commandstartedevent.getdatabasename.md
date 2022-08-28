Повертає базу даних, на якій виконувалась команда

-   [« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName](mongodb-driver-monitoring-commandstartedevent.getcommandname.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId »](mongodb-driver-monitoring-commandstartedevent.getoperationid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)