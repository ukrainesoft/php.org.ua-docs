Повертає, чи сесія була позначена як брудна

-   [« MongoDB\\Driver\\Session::getTransactionState](mongodb-driver-session.gettransactionstate.html)
    
-   [MongoDB\\Driver\\Session::isInTransaction »](mongodb-driver-session.isintransaction.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Повертає, чи сесія була позначена як брудна
    

# MongoDBDriverSession::isDirty

(mongodb >=1.13.0)

MongoDBDriverSession::isDirty - Повертає, чи була сесія позначена як брудна

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::isDirty(): bool
```

Повертає, чи була сесія позначена як брудна (тобто була використана з командою, яка зіткнулася з мережевою помилкою).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція повертає, чи сесія була позначена як брудна.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)