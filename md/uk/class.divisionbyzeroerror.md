- [«AssertionError](class.assertionerror.md)
- [CompileError »](class.compileerror.md)

- [PHP Manual](index.md)
- [Предвизначені винятки](reserved.exceptions.md)
- DivisionByZeroError

# DivisionByZeroError

(PHP 7, PHP 8)

## Вступ

**DivisionByZeroError** викидається при спробі поділити число на
нуль.

## Огляд класів

class **DivisionByZeroError** extends
[ArithmeticError](class.arithmeticerror.md) {

/\* Наслідувані властивості \*/

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

/\* Наслідувані методи \*/

final public [Error::getMessage](error.getmessage.md)(): string

final public [Error::getPrevious](error.getprevious.md)():
?[Throwable](class.throwable.md)

final public [Error::getCode](error.getcode.md)(): int

final public [Error::getFile](error.getfile.md)(): string

final public [Error::getLine](error.getline.md)(): int

final public [Error::getTrace](error.gettrace.md)(): array

final public [Error::getTraceAsString](error.gettraceasstring.md)():
string

public [Error::\_\_toString](error.tostring.md)(): string

private [Error::\_\_clone](error.clone.md)(): void

}
