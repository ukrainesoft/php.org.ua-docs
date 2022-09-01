---
navigation:
  - mongodb-driver-cursorinterface.toarray.html: '« MongoDBDriverCursorInterface::toArray'
  - mongodb-driver-server.construct.html: 'MongoDBDriverServer::construct »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDBDriver
title: Клас MongoDBDriverServer
---
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

Невідомий тип сервера, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

**`MongoDB\Driver\Server::TYPE_STANDALONE`**

Автономний тип сервера, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

**`MongoDB\Driver\Server::TYPE_MONGOS`**

Тип сервера Mongos, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

**`MongoDB\Driver\Server::TYPE_POSSIBLE_PRIMARY`**

Тип набору реплік можливого основного сервера, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

Сервер може бути ідентифікований як можливий основний, якщо він ще не був перевірений, але інша пам'ять реплік набору думає, що він є основним.

**`MongoDB\Driver\Server::TYPE_RS_PRIMARY`**

Тип набору реплік основного сервера, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

**`MongoDB\Driver\Server::TYPE_RS_SECONDARY`**

Тип набору реплік вторинного сервера, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

**`MongoDB\Driver\Server::TYPE_RS_ARBITER`**

Тип набору реплік арбітра сервера, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

**`MongoDB\Driver\Server::TYPE_RS_OTHER`**

Інший тип набору реплік сервера, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

Такі сервери можуть бути приховані, запускаються або відновлюються. Вони можуть бути запитані, але їх списки хостів корисні виявлення поточної конфігурації набору реплік.

**`MongoDB\Driver\Server::TYPE_RS_GHOST`**

Примарний тип набору реплік, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

Сервери можуть бути ідентифіковані як такі, принаймні у трьох ситуаціях: коротко під час запуску сервера; у неініціалізованому наборі реплік; або коли сервер тримається осторонь (тобто видаляється з конфігурації набору реплік). Вони можуть бути запитані, і їх список хостів може бути використаний виявлення поточної конфігурації набору реплік; Однак клієнт може відстежувати цей сервер, сподіваючись, що він переходить у більш корисний стан.

**`MongoDB\Driver\Server::TYPE_LOAD_BALANCER`**

Тип сервера балансувальника навантаження, що повертається [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md)

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.11.0 |  |
| Додано константу **`MongoDB\Driver\Server::TYPE_LOAD_BALANCER`** |  |

## Зміст

-   [MongoDBDriverServer::construct](mongodb-driver-server.construct.md) - Створює новий Server (не використовується)
-   [MongoDBDriverServer::executeBulkWrite](mongodb-driver-server.executebulkwrite.md) — Виконати одну або кілька операцій запису на сервері
-   [MongoDBDriverServer::executeCommand](mongodb-driver-server.executecommand.md) — Виконати команду бази даних на сервері
-   [MongoDBDriverServer::executeQuery](mongodb-driver-server.executequery.md) — Виконує запит до бази даних на сервері
-   [MongoDBDriverServer::executeReadCommand](mongodb-driver-server.executereadcommand.md) - Виконує команду бази даних, яка читає на сервері
-   [MongoDBDriverServer::executeReadWriteCommand](mongodb-driver-server.executereadwritecommand.md) — Виконує команду бази даних, яка читає та пише на сервері
-   [MongoDBDriverServer::executeWriteCommand](mongodb-driver-server.executewritecommand.md) - Виконує команду бази даних, яка пише на сервері
-   [MongoDBDriverServer::getHost](mongodb-driver-server.gethost.md) — Повертає ім'я сервера.
-   [MongoDBDriverServer::getInfo](mongodb-driver-server.getinfo.md) — Повертає масив інформації, що описує сервер
-   [MongoDBDriverServer::getLatency](mongodb-driver-server.getlatency.md) — Повертає затримку сервера у мілісекундах
-   [MongoDBDriverServer::getPort](mongodb-driver-server.getport.md) — Повертає порт, який слухає сервер
-   [MongoDBDriverServer::getServerDescription](mongodb-driver-server.getserverdescription.md) — Повертає ServerDescription сервера
-   [MongoDBDriverServer::getTags](mongodb-driver-server.gettags.md) — Повертає масив тегів, що описують сервер у наборі реплік
-   [MongoDBDriverServer::getType](mongodb-driver-server.gettype.md) — Повертає ціле число, яке означає тип цього сервера
-   [MongoDBDriverServer::isArbiter](mongodb-driver-server.isarbiter.md) — Перевіряє, чи сервер є членом-арбітром у наборі реплік
-   [MongoDBDriverServer::isHidden](mongodb-driver-server.ishidden.md) — Перевіряє, чи сервер є прихованим членом набору реплік
-   [MongoDBDriverServer::isPassive](mongodb-driver-server.ispassive.md) — Перевіряє, чи сервер є пасивним членом набору реплік.
-   [MongoDBDriverServer::isPrimary](mongodb-driver-server.isprimary.md) — Перевіряє, чи сервер є основним членом набору реплік
-   [MongoDBDriverServer::isSecondary](mongodb-driver-server.issecondary.md) — Перевіряє, чи цей сервер є другорядним членом набору реплік.
