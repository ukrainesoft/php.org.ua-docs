Повертає сервери у топології

-   [« MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.html)
    
-   [MongoDB\\Driver\\TopologyDescription::getType »](mongodb-driver-topologydescription.gettype.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.html)
    
-   Повертає сервери у топології
    

# MongoDBDriverTopologyDescription::getServers

(mongodb >=1.13.0)

MongoDBDriverTopologyDescription::getServers — Повертає сервери у топології

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::getServers(): array
```

Повертає масив об'єктів [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.html), що відповідають відомим серверам у топології.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив об'єктів [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.html), що відповідають відомим серверам у топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)