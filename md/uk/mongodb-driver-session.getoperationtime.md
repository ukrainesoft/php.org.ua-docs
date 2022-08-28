Повертає час операції для цього сеансу

-   [« MongoDB\\Driver\\Session::getLogicalSessionId](mongodb-driver-session.getlogicalsessionid.html)
    
-   [MongoDB\\Driver\\Session::getServer »](mongodb-driver-session.getserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Повертає час операції для цього сеансу
    

# MongoDBDriverSession::getOperationTime

(mongodb >=1.4.0)

MongoDBDriverSession::getOperationTime — Повертає час операції для цього сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getOperationTime(): ?MongoDB\BSON\Timestamp
```

Повертає час операції для цього сеансу. Якщо сеанс не використовувався для жодної операції, і [MongoDB\\Driver\\Session::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.html) не був викликаний, час операції буде рівним **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час операції для цього сеансу або **`null`**, якщо сеанс не має часу операції.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Session::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.html) - Збільшує час операції для сеансу