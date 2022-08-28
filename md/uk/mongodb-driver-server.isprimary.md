Перевіряє, чи є сервер основним членом набору реплік

-   [« MongoDB\\Driver\\Server::isPassive](mongodb-driver-server.ispassive.html)
    
-   [MongoDB\\Driver\\Server::isSecondary »](mongodb-driver-server.issecondary.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Перевіряє, чи є сервер основним членом набору реплік
    

# MongoDBDriverServer::isPrimary

(mongodb >=1.0.0)

MongoDBDriverServer::isPrimary — Перевіряє, чи є сервер основним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isPrimary(): bool
```

Повертає, чи є цей сервер [» основным членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-primary) набір реплік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є основним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер