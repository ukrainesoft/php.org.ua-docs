Перевіряє, чи сервер прихованим членом набору реплік

-   [« MongoDBDriverServer::isArbiter](mongodb-driver-server.isarbiter.html)
    
-   [MongoDBDriverServer::isPassive »](mongodb-driver-server.ispassive.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverServer](class.mongodb-driver-server.html)
    
-   Перевіряє, чи сервер прихованим членом набору реплік
    

# MongoDBDriverServer::isHidden

(mongodb >=1.0.0)

MongoDBDriverServer::isHidden — Перевіряє, чи є сервер прихованим членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isHidden(): bool
```

Повертає, чи є цей сервер [» скрытым членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-hidden-member) набір реплік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є прихованим членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер