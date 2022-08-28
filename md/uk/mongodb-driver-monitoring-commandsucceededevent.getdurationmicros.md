Повертає тривалість команди у мікросекундах

-   [« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName](mongodb-driver-monitoring-commandsucceededevent.getcommandname.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId »](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)