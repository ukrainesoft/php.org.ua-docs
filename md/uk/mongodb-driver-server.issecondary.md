Перевіряє, чи є сервер другорядним членом набору реплік

-   [« MongoDB\\Driver\\Server::isPrimary](mongodb-driver-server.isprimary.html)
    
-   [MongoDB\\Driver\\ServerDescription »](class.mongodb-driver-serverdescription.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Перевіряє, чи є сервер другорядним членом набору реплік
    

# MongoDBDriverServer::isSecondary

(mongodb >=1.0.0)

MongoDBDriverServer::isSecondary — Перевіряє, чи є сервер другорядним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isSecondary(): bool
```

Повертає, чи є цей сервер [» второстепенным членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-secondary) набір реплік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є другорядним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер