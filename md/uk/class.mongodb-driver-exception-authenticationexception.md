- [«MongoDB\Driver\Exception](mongodb.exceptions.md)
- [MongoDB\Driver\Exception\BulkWriteException »](class.mongodb-driver-exception-bulkwriteexception.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Exception](mongodb.exceptions.md)
- Клас MongoDB\Driver\Exception\AuthenticationException

# Клас MongoDB\Driver\Exception\AuthenticationException

(mongodb \>= 1.0.0)

## Вступ

Викидається, коли драйвер не може виконати аутентифікацію з
сервером.

## Огляд класів

class **MongoDB\Driver\Exception\AuthenticationException** extends
[MongoDB\Driver\Exception\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
implements
[MongoDB\Driver\Exception\Exception](class.mongodb-driver-exception-exception.md)
{

/\* Наслідувані властивості \*/

protected ?array `$errorLabels`;

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

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
