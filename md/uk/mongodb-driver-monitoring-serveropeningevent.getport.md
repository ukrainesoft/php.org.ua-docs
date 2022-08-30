Повертає порт, на якому прослуховується сервер

-   [« MongoDBDriverMonitoringServerOpeningEvent::getHost](mongodb-driver-monitoring-serveropeningevent.gethost.html)
    
-   [MongoDBDriverMonitoringServerOpeningEvent::getTopologyId »](mongodb-driver-monitoring-serveropeningevent.gettopologyid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.html)
    
-   Повертає порт, на якому прослуховується сервер
    

# MongoDBDriverMonitoringServerOpeningEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerOpeningEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)