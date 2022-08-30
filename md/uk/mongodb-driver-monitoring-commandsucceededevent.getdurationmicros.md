Повертає тривалість команди у мікросекундах

-   [« MongoDBDriverMonitoringCommandSucceededEvent::getCommandName](mongodb-driver-monitoring-commandsucceededevent.getcommandname.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent::getOperationId »](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає тривалість команди у мікросекундах
    

# MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros — Повертає тривалість команди в мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getDurationMicros(): int
```

Тривалість команди - це розраховане значення, яке включає час надсилання повідомлення та отримання відповіді від сервера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тривалість команди у мікросекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)