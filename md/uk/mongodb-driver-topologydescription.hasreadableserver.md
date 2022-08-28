Повертає, чи є у топології сервер, доступний для читання

-   [« MongoDB\\Driver\\TopologyDescription::getType](mongodb-driver-topologydescription.gettype.html)
    
-   [MongoDB\\Driver\\TopologyDescription::hasWritableServer »](mongodb-driver-topologydescription.haswritableserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.html)
    
-   Повертає, чи є у топології сервер, доступний для читання
    

# MongoDBDriverTopologyDescription::hasReadableServer

(mongodb >=1.13.0)

MongoDBDriverTopologyDescription::hasReadableServer — Повертає, чи є в топології сервер, доступний для читання

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::hasReadableServer(?MongoDB\Driver\ReadPreference $readPreference = null): bool
```

Повертає, чи є в топології сервер, доступний для читання, або якщо зазначено параметр `readPreference`, сервер, що відповідає вказаній перевагі читання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає, чи є в топології сервер, доступний для читання, або якщо зазначено параметр `readPreference`, сервер, що відповідає вказаній перевагі читання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)