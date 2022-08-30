Повертає документ команди

-   [« MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   [MongoDBDriverMonitoringCommandStartedEvent::getCommandName »](mongodb-driver-monitoring-commandstartedevent.getcommandname.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає документ команди
    

# MongoDBDriverMonitoringCommandStartedEvent::getCommand

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getCommand — Повертає документ команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getCommand(): object
```

Документ відповіді буде перетворено з BSON в PHP, використовуючи правила [десериализации](mongodb.persistence.deserialization.html) (наприклад, документи BSON будуть перетворені на stdClass).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ команди у вигляді об'єкту **stdClass**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)
-   [Постійні дані](mongodb.persistence.html)