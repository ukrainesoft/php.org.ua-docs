Повертає сервери у топології

-   [« MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.html)
    
-   [MongoDBDriverTopologyDescription::getType »](mongodb-driver-topologydescription.gettype.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.html)
    
-   Повертає сервери у топології
    

# MongoDBDriverTopologyDescription::getServers

(mongodb >=1.13.0)

MongoDBDriverTopologyDescription::getServers — Повертає сервери у топології

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::getServers(): array
```

Повертає масив об'єктів [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html), що відповідають відомим серверам у топології.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив об'єктів [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html), що відповідають відомим серверам у топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)