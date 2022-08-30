Повертає, чи є у топології сервер, доступний для читання

-   [« MongoDBDriverTopologyDescription::getType](mongodb-driver-topologydescription.gettype.html)
    
-   [MongoDBDriverTopologyDescription::hasWritableServer »](mongodb-driver-topologydescription.haswritableserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)