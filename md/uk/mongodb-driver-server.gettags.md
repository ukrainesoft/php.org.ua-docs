Повертає масив тегів, що описують сервер у наборі реплік

-   [« MongoDB\\Driver\\Server::getServerDescription](mongodb-driver-server.getserverdescription.html)
    
-   [MongoDB\\Driver\\Server::getType »](mongodb-driver-server.gettype.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Повертає масив тегів, що описують сервер у наборі реплік
    

# MongoDBDriverServer::getTags

(mongodb >=1.0.0)

MongoDBDriverServer::getTags — Повертає масив тегів, що описують сервер у наборі реплік

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getTags(): array
```

Повертає array [» тегов](https://www.mongodb.com/docs/manual/reference/glossary/#term-tag), що використовуються для опису цього сервера в наборі реплік. Масив буде містити нуль або більше пар string ключів та значень.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає array теги, що використовуються для опису сервера в наборі реплік.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер