Повертає час операції для цього сеансу

-   [« MongoDBDriverSession::getLogicalSessionId](mongodb-driver-session.getlogicalsessionid.html)
    
-   [MongoDBDriverSession::getServer »](mongodb-driver-session.getserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverSession](class.mongodb-driver-session.html)
    
-   Повертає час операції для цього сеансу
    

# MongoDBDriverSession::getOperationTime

(mongodb >=1.4.0)

MongoDBDriverSession::getOperationTime — Повертає час операції для цього сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getOperationTime(): ?MongoDB\BSON\Timestamp
```

Повертає час операції для цього сеансу. Якщо сеанс не використовувався для жодної операції, і [MongoDBDriverSession::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.html) не був викликаний, час операції буде рівним **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час операції для цього сеансу або **`null`**, якщо сеанс не має часу операції.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverSession::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.html) - Збільшує час операції для сеансу