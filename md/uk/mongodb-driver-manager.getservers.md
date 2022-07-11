- [« MongoDB\Driver\Manager::getReadPreference](mongodb-driver-manager.getreadpreference.md)
- [MongoDB\Driver\Manager::getWriteConcern »](mongodb-driver-manager.getwriteconcern.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Manager](class.mongodb-driver-manager.md)
- Повертає сервери, до яких підключено менеджера

# MongoDB\Driver\Manager::getServers

(mongodb \>=1.0.0)

MongoDB\Driver\Manager::getServers - Повертає сервери, до яких
підключений менеджер

### Опис

final public **MongoDB\Driver\Manager::getServers**(): array

Повертає масив (array) екземплярів
[MongoDB\Driver\Server](class.mongodb-driver-server.md), до яких
підключений поточний менеджер.

> **Примітка**: Оскільки драйвер підключається до бази даних ліниво,
> цей метод може повертати порожній масив (array), якщо він викликається
> перед виконанням операції
> [MongoDB\Driver\Manager](class.mongodb-driver-manager.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array) екземплярів
[MongoDB\Driver\Server](class.mongodb-driver-server.md), до яких
підключений менеджер.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\Manager::getServers()****

` <?php$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");/* З-за того, драйвер підключається к серверу ліниво, дзвін Manager порожній масив. */var_dump($manager->getServers());$command = new MongoDB\Driver\Command(['ping' => 1]);$manager->executeCommand('db', $command);var_dump($ manager->getServers());?> `

Результатом виконання цього прикладу буде щось подібне:

array(0) {
}
array(1) {
[0]=>
object(MongoDB\Driver\Server)#3 (10) {
["host"]=>
string(9) "localhost"
["port"]=>
int(27017)
["type"]=>
int(1)
["is_primary"]=>
bool(false)
["is_secondary"]=>
bool(false)
["is_arbiter"]=>
bool(false)
["is_hidden"]=>
bool(false)
["is_passive"]=>
bool(false)
["last_hello_response"]=>
array(8) {
["isWritablePrimary"]=>
bool(true)
["maxBsonObjectSize"]=>
int(16777216)
["maxMessageSizeBytes"]=>
int(48000000)
["maxWriteBatchSize"]=>
int(1000)
["localTime"]=>
object(MongoDB\BSON\UTCDateTime)#4 (1) {
["milliseconds"]=>
int(1447267964517)
}
["maxWireVersion"]=>
int(3)
["minWireVersion"]=>
int(0)
["ok"]=>
float(1)
}
["round_trip_time"]=>
int(554)
}
}

### Дивіться також

- [MongoDB\Driver\Server](class.mongodb-driver-server.md)
- [MongoDB\Driver\Manager::selectServer()](mongodb-driver-manager.selectserver.md) -
Вибрати сервер, що відповідає перевагам читання
