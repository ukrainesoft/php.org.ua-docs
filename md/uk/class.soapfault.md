- [« SoapServer::setPersistence](soapserver.setpersistence.md)
- [SoapFault::\_\_construct »](soapfault.construct.md)

- [PHP Manual](index.md)
- [SOAP](book.soap.md)
- Клас SoapFault

# Клас SoapFault

(PHP 5, PHP 7, PHP 8)

## Вступ

Помилка SOAP.

## Огляд класів

class **SoapFault** extends [Exception](class.exception.md) {

/\* Властивості \*/

public string `$faultstring`;

public ?string `$faultcode` = null;

public ?string `$faultcodens` = null;

public ?string `$faultactor` = null;

public
[mixed](language.types.declarations.md#language.types.declarations.mixed)
$detail = null;

public ?string `$_name` = null;

public
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$headerfault` = null;

/\* Наслідувані властивості \*/

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

/\* Методи \*/

public [\_\_construct](soapfault.construct.md)(
array\|string\|null `$code`,
string `$string`,
?string `$actor` = **`null`**,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$details` = **`null`**,
?string `$name` = **`null`**,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$headerFault` = **`null`**
)

public [\_\_toString](soapfault.tostring.md)(): string

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

## Властивості

`_name`

`detail`

`faultactor`

`faultcode`

`faultcodens`

`faultstring`

`headerfault`

## Зміст

- [SoapFault::\_\_construct](soapfault.construct.md) - Конструктор
SoapFault
- [SoapFault::\_\_toString](soapfault.tostring.md) — Отримати
текстове уявлення SoapFault
