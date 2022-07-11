- [« PharFileInfo::setMetadata](pharfileinfo.setmetadata.md)
- [Rar »](book.rar.md)

- [PHP Manual](index.md)
- [Phar](book.phar.md)
- Клас PharException

# Клас PharException

(PHP 5 = 5.3.0, PHP 7, PHP 8, PECL phar = 1.0.0)

## Вступ

Клас PharException надає клас виключення модуля phar для
блоків try/catch.

## Огляд класів

class **PharException** extends [Exception](class.exception.md) {

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
