Повертає виняток, пов'язаний із невдалою командою

-   [« MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros](mongodb-driver-monitoring-commandfailedevent.getdurationmicros.html)
    
-   [MongoDBDriverMonitoringCommandFailedEvent::getOperationId »](mongodb-driver-monitoring-commandfailedevent.getoperationid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
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

Повертає виняток ([Exception](class.exception.md)), пов'язане з невдалою командою.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)