Перевіряє, чи є сервер пасивним членом набору реплік.

-   [« MongoDB\\Driver\\Server::isHidden](mongodb-driver-server.ishidden.html)
    
-   [MongoDB\\Driver\\Server::isPrimary »](mongodb-driver-server.isprimary.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Перевіряє, чи є сервер пасивним членом набору реплік.
    

# MongoDBDriverServer::isPassive

(mongodb >=1.0.0)

MongoDBDriverServer::isPassive — Перевіряє, чи є сервер пасивним членом набору реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::isPassive(): bool
```

Повертає, чи є цей сервер [» пассивным членом](https://www.mongodb.com/docs/manual/reference/glossary/#term-passive-member) набору реплік (тобто його пріоритет дорівнює `0`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цей сервер є пасивним членом набору реплік, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер