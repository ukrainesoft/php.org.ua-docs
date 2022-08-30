Повертає налаштування поточної транзакції

-   [« MongoDBDriverSession::getServer](mongodb-driver-session.getserver.html)
    
-   [MongoDBDriverSession::getTransactionState »](mongodb-driver-session.gettransactionstate.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverSession](class.mongodb-driver-session.html)
    
-   Повертає налаштування поточної транзакції
    

# MongoDBDriverSession::getTransactionOptions

(mongodb >=1.7.0)

MongoDBDriverSession::getTransactionOptions — Повертає установки поточної транзакції

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getTransactionOptions(): ?array
```

Повертає установки поточної транзакції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить налаштування поточної транзакції, або \*\*`null`\*\*якщо транзакція не стартована.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverSession::getTransactionState()](mongodb-driver-session.gettransactionstate.html) - Повертає статус транзакції для поточної сесії