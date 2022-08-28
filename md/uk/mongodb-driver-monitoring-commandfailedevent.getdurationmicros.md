Повертає тривалість команди у мікросекундах

-   [« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName](mongodb-driver-monitoring-commandfailedevent.getcommandname.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError »](mongodb-driver-monitoring-commandfailedevent.geterror.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   Повертає тривалість команди у мікросекундах
    

# MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros — Повертає тривалість команди в мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getDurationMicros(): int
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