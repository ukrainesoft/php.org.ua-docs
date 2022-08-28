Повертає виняток, пов'язаний із невдалою командою

-   [« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros](mongodb-driver-monitoring-commandfailedevent.getdurationmicros.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId »](mongodb-driver-monitoring-commandfailedevent.getoperationid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   Повертає виняток, пов'язаний із невдалою командою
    

# MongoDBDriverMonitoringCommandFailedEvent::getError

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getError — Повертає виняток, пов'язаний із невдалою командою

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getError(): Exception
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виняток ([Exception](class.exception.html)), пов'язане з невдалою командою.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)