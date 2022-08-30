Повертає рядок, що позначає тип топології

-   [« MongoDBDriverTopologyDescription::getServers](mongodb-driver-topologydescription.getservers.html)
    
-   [MongoDBDriverTopologyDescription::hasReadableServer »](mongodb-driver-topologydescription.hasreadableserver.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.html)
    
-   Повертає рядок, що позначає тип топології
    

# MongoDBDriverTopologyDescription::getType

(mongodb >=1.13.0)

MongoDBDriverTopologyDescription::getType — Повертає рядок, що позначає тип топології

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::getType(): string
```

Повертає рядок (string), що означає тип топології. Значення співвідноситиметься з константою [MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що означає тип топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)