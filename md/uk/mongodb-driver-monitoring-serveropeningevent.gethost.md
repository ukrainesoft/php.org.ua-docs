Повертає ім'я сервера хоста

-   [« MongoDB\\Driver\\Monitoring\\ServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort »](mongodb-driver-monitoring-serveropeningevent.getport.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.html)
    
-   Повертає ім'я сервера хоста
    

# MongoDBDriverMonitoringServerOpeningEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerOpeningEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)