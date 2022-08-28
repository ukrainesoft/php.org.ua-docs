Повертає час кластера для цього сеансу

-   [« MongoDB\\Driver\\Session::endSession](mongodb-driver-session.endsession.html)
    
-   [MongoDB\\Driver\\Session::getLogicalSessionId »](mongodb-driver-session.getlogicalsessionid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Повертає час кластера для цього сеансу
    

# MongoDBDriverSession::getClusterTime

(mongodb >=1.4.0)

MongoDBDriverSession::getClusterTime — Повертає час кластера для цього сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getClusterTime(): ?object
```

Повертає час кластера для цього сеансу. Якщо сеанс не використовувався для будь-якої операції та [MongoDB\\Driver\\Session::advanceClusterTime()](mongodb-driver-session.advanceclustertime.html) не був викликаний, час кластера буде рівний **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час кластера для цього сеансу або **`null`**, якщо сеанс не має часу кластера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Session::advanceClusterTime()](mongodb-driver-session.advanceclustertime.html) - Збільшує час кластера для сеансу