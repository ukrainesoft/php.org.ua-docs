Повертає логічний ідентифікатор сеансу для цього сеансу

-   [« MongoDBDriverSession::getClusterTime](mongodb-driver-session.getclustertime.html)
    
-   [MongoDBDriverSession::getOperationTime »](mongodb-driver-session.getoperationtime.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverSession](class.mongodb-driver-session.html)
    
-   Повертає логічний ідентифікатор сеансу для цього сеансу
    

# MongoDBDriverSession::getLogicalSessionId

(mongodb >=1.4.0)

MongoDBDriverSession::getLogicalSessionId — Повертає логічний ідентифікатор сеансу для цього сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getLogicalSessionId(): object
```

Повертає логічний ідентифікатор сеансу для цього сеансу, який можна використовувати для ідентифікації операцій сеансу на сервері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає логічний ідентифікатор сеансу цього сеансу.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)