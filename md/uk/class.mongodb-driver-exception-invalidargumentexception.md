- [« MongoDB\Driver\Exception\ExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.md)
- [MongoDB\Driver\Exception\LogicException »](class.mongodb-driver-exception-logicexception.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Exception](mongodb.exceptions.md)
- Клас MongoDB\Driver\Exception\InvalidArgumentException

# Клас MongoDB\Driver\Exception\InvalidArgumentException

(mongodb \>= 1.0.0)

## Вступ

Викидається, коли методу драйвера передано некоректні аргументи
(наприклад, неприпустимі типи опцій).

## Огляд класів

class **MongoDB\Driver\Exception\InvalidArgumentException** extends
[InvalidArgumentException](class.invalidargumentexception.md)
implements
[MongoDB\Driver\Exception\Exception](class.mongodb-driver-exception-exception.md)
{

/\* Наслідувані властивості \*/

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

/\* Наслідувані методи \*/

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
