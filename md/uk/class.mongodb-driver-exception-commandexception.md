- [« MongoDB\Driver\Exception\BulkWriteException](class.mongodb-driver-exception-bulkwriteexception.md)
- [MongoDB\Driver\Exception\CommandException::getResultDocument »](mongodb-driver-commandexception.getresultdocument.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Exception](mongodb.exceptions.md)
- Клас MongoDB\Driver\Exception\CommandException

# Клас MongoDB\Driver\Exception\CommandException

(mongodb \>= 1.5.0)

## Вступ

Викидається, у разі помилки команди.

## Огляд класів

abstract class **MongoDB\Driver\Exception\CommandException** extends
[MongoDB\Driver\Exception\ServerException](class.mongodb-driver-exception-serverexception.md)
implements
[MongoDB\Driver\Exception\Exception](class.mongodb-driver-exception-exception.md)
{

/\* Властивості \*/

protected object `$resultDocument`;

/\* Наслідувані властивості \*/

protected ?array `$errorLabels`;

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

/\* Методи \*/

final public
[getResultDocument](mongodb-driver-commandexception.getresultdocument.md)():
object

/\* Наслідувані методи \*/

final public
[MongoDB\Driver\Exception\RuntimeException::hasErrorLabel](mongodb-driver-runtimeexception.haserrorlabel.md)(string
`$errorLabel`): bool

final public [Exception::getMessage](exception.getmessage.md)():
string

final public [Exception::getPrevious](exception.getprevious.md)():
?[Throwable](class.throwable.md)

final public [Exception::getCode](exception.getcode.md)(): int

final public [Exception::getFile](exception.getfile.md)(): string

final public [Exception::getLine](exception.getline.md)(): int

final public [Exception::getTrace](exception.gettrace.md)(): array

final public
[Exception::getTraceAsString](exception.gettraceasstring.md)(): string

public [Exception::\_\_toString](exception.tostring.md)(): string

private [Exception::\_\_clone](exception.clone.md)(): void

}

## Властивості

`resultDocument`
Документ результату, пов'язаний із невдалою командою.

## Зміст

- [MongoDB\Driver\Exception\CommandException::getResultDocument](mongodb-driver-commandexception.getresultdocument.md)
— Повертає результат документа для невдалої команди
