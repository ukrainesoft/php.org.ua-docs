- [«UI\Key](class.ui-key.md)
- [UI\Exception\RuntimeException »](class.ui-exception-runtimeexception.md)

- [PHP Manual](index.md)
- [UI](book.ui.md)
- InvalidArgumentException

# InvalidArgumentException

(UI 1.0.3)

## Вступ

## Огляд класів

class **UI\Exception\InvalidArgumentException** extends
[InvalidArgumentException](class.invalidargumentexception.md)
implements [Throwable](class.throwable.md) {

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
