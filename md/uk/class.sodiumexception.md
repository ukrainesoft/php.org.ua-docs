- [« sodium_unpad](function.sodium-unpad.md)
- [Модулі для роботи з базами даних»](refs.database.md)

- [PHP Manual](index.md)
- [Sodium](book.sodium.md)
- Клас SodiumException

# Клас SodiumException

(PHP 7 \>= 7.2.0, PHP 8)

## Вступ

Винятки, що викидаються функціями sodium.

## Огляд класів

class **SodiumException** extends [Exception](class.exception.md) {

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
