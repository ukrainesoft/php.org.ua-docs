- [« FFI\CType::getStructFieldType](ffi-ctype.getstructfieldtype.md)
- [FFI\ParserException »](class.ffi-parserexception.md)

- [PHP Manual](index.md)
- [FFI](book.ffi.md)
- Винятки FFI

# Винятки FFI

(PHP 7 \>= 7.4.0, PHP 8)

## Вступ

## Огляд класів

class **FFI\Exception** extends [Error](class.error.md) {

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
