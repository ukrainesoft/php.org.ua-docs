- [« MongoDB\Driver\Manager::startSession](mongodb-driver-manager.startsession.md)
- [MongoDB\Driver\Command::\_\_construct »](mongodb-driver-command.construct.md)

- [PHP Manual](index.md)
- [MongoDB\Driver](book.mongodb.md)
- Клас The MongoDB\Driver\Command

# Клас The MongoDB\Driver\Command

(mongodb \>=1.0.0)

## Вступ

Клас **MongoDB\Driver\Command** - це об'єкт значення, що представляє
команда бази даних.

Щоб надати "Помічників команд (Command Helpers)" має бути
створено об'єкт **MongoDB\Driver\Command**.

## Огляд класів

final class **MongoDB\Driver\Command** {

/\* Методи \*/

final public
[\_\_construct](mongodb-driver-command.construct.md)(array\|object
`$document`, array `$commandOptions` = ?)

}

## Приклади

**Приклад #1 Використання **MongoDB\Driver\Command** для надання
помічника зі створення колекцій**

`<?phpclass CreateCollection {    protected $cmd = array(); function __construct($collectionName) {         $this->cmd["create"] = (string)$collectionName; }    function setCappedCollection($maxBytes, $maxDocuments = false) {        $this->cmd["capped"] = true; $this->cmd["size"]   = (int)$maxBytes; if ($maxDocuments) {             $this->cmd["max"] = (int)$maxDocuments; }    }   function usePowerOf2Sizes($bool) {       if ($bool) {             $this->cm|| } else {             $this->cmd["flags"] = 0; }    }    function setFlags($flags) {        $this->cmd["flags"] = (int)$flags; }   function getCommand() {       return new MongoDB\Driver\Command($this->cmd); }   function getCollectionName() {        return $this->cmd["create"]; }}$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");$createCollection = new CreateCollection("cappedCollection");$createCollection->setCappedCollection(64 *                $createCollection->getCommand(); $cursor==$manager->executeCommand("databaseName", $command); $response==$cursor->toArray()[0]; var_dump($response); $collstats==["collstats"==>$createCollection->getCollectionName()]; $cursor==$manager->executeCommand("databaseName", new|MongoDB\Driver\Command($collstats)); $response==$cursor->toArray()[0]; var_dump($response);} catch(MongoDB\Driver\Exception $e) {    echo $e->getMessage(), "
";   exit;}?> `

Результат виконання цього прикладу:

object(MongoDB\Driver\Command)#3 (1) {
["command"]=>
array(3) {
["create"]=>
string(16) "cappedCollection"
["capped"]=>
bool(true)
["size"]=>
int(65536)
}
}
array(1) {
["ok"]=>
float(1)
}
array(16) {
["ns"]=>
string(29) "databaseName.cappedCollection"
["count"]=>
int(0)
["size"]=>
int(0)
["numExtents"]=>
int(1)
["storageSize"]=>
int(65536)
["nindexes"]=>
int(1)
["lastExtentSize"]=>
float(65536)
["paddingFactor"]=>
float(1)
["paddingFactorNote"]=>
string(101) "paddingFactor is unused and unmaintained in 2.8. It remains hard coded to 1.0 for compatibility only."
["userFlags"]=>
int(0)
["capped"]=>
bool(true)
["max"]=>
int(9223372036854775807)
["maxSize"]=>
int(65536)
["totalIndexSize"]=>
int(8176)
["indexSizes"]=>
object(stdClass)#4 (1) {
["_id_"]=>
int(8176)
}
["ok"]=>
float(1)
}

## Зміст

- [MongoDB\Driver\Command::\_\_construct](mongodb-driver-command.construct.md)
— Створює новий об'єкт Command
