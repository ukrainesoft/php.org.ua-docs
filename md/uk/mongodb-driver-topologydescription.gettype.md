Повертає рядок, що позначає тип топології

-   [« MongoDB\\Driver\\TopologyDescription::getServers](mongodb-driver-topologydescription.getservers.html)
    
-   [MongoDB\\Driver\\TopologyDescription::hasReadableServer »](mongodb-driver-topologydescription.hasreadableserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.html)
    
-   Повертає рядок, що позначає тип топології
    

# MongoDBDriverTopologyDescription::getType

(mongodb >=1.13.0)

MongoDBDriverTopologyDescription::getType — Повертає рядок, що позначає тип топології

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::getType(): string
```

Повертає рядок (string), що означає тип топології. Значення співвідноситиметься з константою [MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що означає тип топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)