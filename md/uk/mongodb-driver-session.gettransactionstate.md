Повертає статус транзакції для поточної сесії

-   [« MongoDB\\Driver\\Session::getTransactionOptions](mongodb-driver-session.gettransactionoptions.html)
    
-   [MongoDB\\Driver\\Session::isDirty »](mongodb-driver-session.isdirty.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Повертає статус транзакції для поточної сесії
    

# MongoDBDriverSession::getTransactionState

(mongodb >=1.7.0)

MongoDBDriverSession::getTransactionState — Повертає статус транзакції для поточної сесії

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getTransactionState(): string
```

Повертає статус транзакції для сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає статус транзакції для сесії.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Session::isInTransaction()](mongodb-driver-session.isintransaction.html) - Визначає, чи відбувається зараз багатодокументна транзакція
-   [MongoDB\\Driver\\Session::getTransactionOptions()](mongodb-driver-session.gettransactionoptions.html) - Повертає налаштування поточної транзакції