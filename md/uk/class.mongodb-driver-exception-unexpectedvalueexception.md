- [« MongoDB\Driver\Exception\SSLConnectionException](class.mongodb-driver-exception-sslconnectionexception.md)
- [MongoDB\Driver\Exception\WriteException »](class.mongodb-driver-exception-writeexception.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Exception](mongodb.exceptions.md)
- Клас MongoDB\Driver\Exception\UnexpectedValueException

# Клас MongoDB\Driver\Exception\UnexpectedValueException

(mongodb \>= 1.0.0)

## Вступ

Викидається, коли драйвер стикається з несподіваним значенням
(наприклад, під час серіалізації або десеріалізації BSON).

## Огляд класів

class **MongoDB\Driver\Exception\UnexpectedValueException** extends
[UnexpectedValueException](class.unexpectedvalueexception.md)
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
