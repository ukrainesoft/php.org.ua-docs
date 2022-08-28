Клас MongoDBDriverServer

-   [« MongoDB\\Driver\\CursorInterface::toArray](mongodb-driver-cursorinterface.toarray.html)
    
-   [MongoDB\\Driver\\Server::\_\_construct »](mongodb-driver-server.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver](book.mongodb.html)
    
-   Клас MongoDBDriverServer
    

# Клас MongoDBDriverServer

(mongodb >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\Server
     
     {

    /* Константы */
    
     const
     int
      TYPE_UNKNOWN = 0;

    const
     int
      TYPE_STANDALONE = 1;

    const
     int
      TYPE_MONGOS = 2;

    const
     int
      TYPE_POSSIBLE_PRIMARY = 3;

    const
     int
      TYPE_RS_PRIMARY = 4;

    const
     int
      TYPE_RS_SECONDARY = 5;

    const
     int
      TYPE_RS_ARBITER = 6;

    const
     int
      TYPE_RS_OTHER = 7;

    const
     int
      TYPE_RS_GHOST = 8;

    const
     int
      TYPE_LOAD_BALANCER = 9;


    /* Методы */
    
   final private __construct()
final public executeBulkWrite(string $namespace, MongoDB\Driver\BulkWrite $bulk, array|MongoDB\Driver\WriteConcern|null $options = null): MongoDB\Driver\WriteResult
final public executeCommand(string $db, MongoDB\Driver\Command $command, array|MongoDB\Driver\ReadPreference|null $options = null): MongoDB\Driver\Cursor
final public executeQuery(string $namespace, MongoDB\Driver\Query $query, array|MongoDB\Driver\ReadPreference|null $options = null): MongoDB\Driver\Cursor
final public executeReadCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
final public executeReadWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
final public executeWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
final public getHost(): string
final public getInfo(): array
final public getLatency(): ?integer
final public getPort(): int
final public getServerDescription(): MongoDB\Driver\ServerDescription
final public getTags(): array
final public getType(): int
final public isArbiter(): bool
final public isHidden(): bool
final public isPassive(): bool
final public isPrimary(): bool
final public isSecondary(): bool

   }
```

## Обумовлені константи

**`MongoDB\Driver\Server::TYPE_UNKNOWN`**

Невідомий тип сервера, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

**`MongoDB\Driver\Server::TYPE_STANDALONE`**

Автономний тип сервера, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

**`MongoDB\Driver\Server::TYPE_MONGOS`**

Тип сервера Mongos, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

**`MongoDB\Driver\Server::TYPE_POSSIBLE_PRIMARY`**

Тип набору реплік можливого основного сервера, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

Сервер може бути ідентифікований як можливий основний, якщо він ще не був перевірений, але інша пам'ять реплік набору думає, що він є основним.

**`MongoDB\Driver\Server::TYPE_RS_PRIMARY`**

Тип набору реплік основного сервера, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

**`MongoDB\Driver\Server::TYPE_RS_SECONDARY`**

Тип набору реплік вторинного сервера, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

**`MongoDB\Driver\Server::TYPE_RS_ARBITER`**

Тип набору реплік арбітра сервера, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

**`MongoDB\Driver\Server::TYPE_RS_OTHER`**

Інший тип набору реплік сервера, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

Такі сервери можуть бути приховані, запускаються або відновлюються. Вони можуть бути запитані, але їх списки хостів корисні виявлення поточної конфігурації набору реплік.

**`MongoDB\Driver\Server::TYPE_RS_GHOST`**

Примарний тип набору реплік, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

Сервери можуть бути ідентифіковані як такі, принаймні у трьох ситуаціях: коротко під час запуску сервера; у неініціалізованому наборі реплік; або коли сервер тримається осторонь (тобто видаляється з конфігурації набору реплік). Вони можуть бути запитані, і їх список хостів може бути використаний виявлення поточної конфігурації набору реплік; Однак клієнт може відстежувати цей сервер, сподіваючись, що він переходить у більш корисний стан.

**`MongoDB\Driver\Server::TYPE_LOAD_BALANCER`**

Тип сервера балансувальника навантаження, що повертається [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.html)

## список змін

| Версия                                                           | Описание |
|------------------------------------------------------------------|----------|
| PECL mongodb 1.11.0                                              |          |
| Додано константу **`MongoDB\Driver\Server::TYPE_LOAD_BALANCER`** |          |

## Зміст

-   [MongoDB\\Driver\\Server::\_\_construct](mongodb-driver-server.construct.html) - Створює новий Server (не використовується)
-   [MongoDB\\Driver\\Server::executeBulkWrite](mongodb-driver-server.executebulkwrite.html) — Виконати одну або кілька операцій запису на сервері
-   [MongoDB\\Driver\\Server::executeCommand](mongodb-driver-server.executecommand.html) — Виконати команду бази даних на сервері
-   [MongoDB\\Driver\\Server::executeQuery](mongodb-driver-server.executequery.html) — Виконує запит до бази даних на сервері
-   [MongoDB\\Driver\\Server::executeReadCommand](mongodb-driver-server.executereadcommand.html) - Виконує команду бази даних, яка читає на сервері
-   [MongoDB\\Driver\\Server::executeReadWriteCommand](mongodb-driver-server.executereadwritecommand.html) — Виконує команду бази даних, яка читає та пише на сервері
-   [MongoDB\\Driver\\Server::executeWriteCommand](mongodb-driver-server.executewritecommand.html) - Виконує команду бази даних, яка пише на сервері
-   [MongoDB\\Driver\\Server::getHost](mongodb-driver-server.gethost.html) — Повертає ім'я сервера.
-   [MongoDB\\Driver\\Server::getInfo](mongodb-driver-server.getinfo.html) — Повертає масив інформації, що описує сервер
-   [MongoDB\\Driver\\Server::getLatency](mongodb-driver-server.getlatency.html) — Повертає затримку сервера у мілісекундах
-   [MongoDB\\Driver\\Server::getPort](mongodb-driver-server.getport.html) — Повертає порт, який слухає сервер
-   [MongoDB\\Driver\\Server::getServerDescription](mongodb-driver-server.getserverdescription.html) — Повертає ServerDescription сервера
-   [MongoDB\\Driver\\Server::getTags](mongodb-driver-server.gettags.html) — Повертає масив тегів, що описують сервер у наборі реплік
-   [MongoDB\\Driver\\Server::getType](mongodb-driver-server.gettype.html) — Повертає ціле число, яке означає тип цього сервера
-   [MongoDB\\Driver\\Server::isArbiter](mongodb-driver-server.isarbiter.html) — Перевіряє, чи сервер є членом-арбітром у наборі реплік
-   [MongoDB\\Driver\\Server::isHidden](mongodb-driver-server.ishidden.html) — Перевіряє, чи сервер є прихованим членом набору реплік
-   [MongoDB\\Driver\\Server::isPassive](mongodb-driver-server.ispassive.html) — Перевіряє, чи сервер є пасивним членом набору реплік.
-   [MongoDB\\Driver\\Server::isPrimary](mongodb-driver-server.isprimary.html) — Перевіряє, чи сервер є основним членом набору реплік
-   [MongoDB\\Driver\\Server::isSecondary](mongodb-driver-server.issecondary.html) — Перевіряє, чи цей сервер є другорядним членом набору реплік.