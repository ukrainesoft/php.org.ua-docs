Перевіряє, чи є сервер другорядним членом набору реплік

-   [« MongoDBDriverServer::isPrimary](mongodb-driver-server.isprimary.html)
    
-   [MongoDBDriverServerDescription »](class.mongodb-driver-serverdescription.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverServer](class.mongodb-driver-server.html)
    
-   Перевіряє, чи є сервер другорядним членом набору реплік
    

# MongoDBDriverServer::isSecondary

(mongodb >=1.0.0)

MongoDBDriverServer::isSecondary — Перевіряє, чи є сервер другорядним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isSecondary(): bool
```

Повертає, чи є цей сервер [» другорядним членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-secondary) набір реплік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є другорядним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер