Повертає порт, на якому прослуховується сервер

-   [« MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost](mongodb-driver-monitoring-serverclosedevent.gethost.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId »](mongodb-driver-monitoring-serverclosedevent.gettopologyid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html)
    
-   Повертає порт, на якому прослуховується сервер
    

# MongoDBDriverMonitoringServerClosedEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerClosedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)