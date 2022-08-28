Повертає ім'я команди

-   [« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand](mongodb-driver-monitoring-commandstartedevent.getcommand.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName »](mongodb-driver-monitoring-commandstartedevent.getdatabasename.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає ім'я команди
    

# MongoDBDriverMonitoringCommandStartedEvent::getCommandName

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getCommandName — Повертає ім'я команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getCommandName(): string
```

Повертає ім'я команди (наприклад, `"find"` `"aggregate"`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)