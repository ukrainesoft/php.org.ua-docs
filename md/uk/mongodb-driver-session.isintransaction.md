Визначає, чи відбувається зараз багатодокументна транзакція.

-   [« MongoDBDriverSession::isDirty](mongodb-driver-session.isdirty.html)
    
-   [MongoDBDriverSession::startTransaction »](mongodb-driver-session.starttransaction.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverSession](class.mongodb-driver-session.html)
    
-   Визначає, чи відбувається зараз багатодокументна транзакція.
    

# MongoDBDriverSession::isInTransaction

(mongodb >=1.6.0)

MongoDBDriverSession::isInTransaction — Визначає, чи відбувається багатодокументна транзакція.

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::isInTransaction(): boolean
```

Визначає, чи відбувається зараз у поточній сесії багатодокументна транзакція. Вважається, що транзакція "відбувається прямо зараз", якщо вона була запущена, але поки не була підтверджена ні скасована.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverSession::getTransactionState()](mongodb-driver-session.gettransactionstate.html) - Повертає статус транзакції для поточної сесії