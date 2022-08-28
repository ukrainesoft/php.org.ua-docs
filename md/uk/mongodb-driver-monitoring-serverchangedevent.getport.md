Повертає порт, на якому прослуховується сервер

-   [« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription](mongodb-driver-monitoring-serverchangedevent.getnewdescription.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPreviousDescription »](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
    
-   Повертає порт, на якому прослуховується сервер
    

# MongoDBDriverMonitoringServerChangedEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)