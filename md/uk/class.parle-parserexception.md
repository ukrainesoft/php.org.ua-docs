- [« Parle\LexerException](class.parle-lexerexception.md)
- [PCRE »](book.pcre.md)

- [PHP Manual](index.md)
- [Parle](book.parle.md)
- Клас Parle\ParserException

# Клас Parle\ParserException

(PECL parle \>= 0.5.1)

## Вступ

## Огляд класів

class **Parle\ParserException** extends
[Exception](class.exception.md) implements
[Throwable](class.throwable.md) {

/\* Наслідувані властивості \*/

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

/\* Методи \*/

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
