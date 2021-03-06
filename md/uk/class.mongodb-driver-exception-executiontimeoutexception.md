- [« MongoDB\Driver\Exception\Exception](class.mongodb-driver-exception-exception.md)
- [MongoDB\Driver\Exception\InvalidArgumentException »](class.mongodb-driver-exception-invalidargumentexception.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Exception](mongodb.exceptions.md)
- Клас MongoDB\Driver\Exception\ExecutionTimeoutException

# Клас MongoDB\Driver\Exception\ExecutionTimeoutException

(mongodb \>= 1.0.0)

## Вступ

Викидається, коли запит або команда не завершується протягом
певного періоду часу (наприклад,
[» maxTimeMS](https://www.mongodb.com/docs/manual/tutorial/terminate-running-operations/#maxtimems)).

## Огляд класів

final class **MongoDB\Driver\Exception\ExecutionTimeoutException**
extends
[MongoDB\Driver\Exception\ServerException](class.mongodb-driver-exception-serverexception.md)
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

## Список змін

| Версія                                                                                                                                                                                                                                            | Опис |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| PECL mongodb 1.5.0 Тепер цей клас розширює [MongoDB\Driver\Exception\ServerException](class.mongodb-driver-exception-serverexception.md) замість [MongoDB\Driver\Exception\RuntimeException](class.mongodb-driver-exception-runtimeexception.md). |      |
