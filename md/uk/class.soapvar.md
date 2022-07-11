- [« SoapParam::\_\_construct](soapparam.construct.md)
- [SoapVar::\_\_construct »](soapvar.construct.md)

- [PHP Manual](index.md)
- [SOAP](book.soap.md)
- Клас SoapVar

# Клас SoapVar

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас, що представляє змінну або об'єкт для використання з
сервісами SOAP.

## Огляд класів

class **SoapVar** {

/\* Властивості \*/

public int `$enc_type`;

public
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$enc_value` = null;

public ?string `$enc_stype` = null;

public ?string `$enc_ns` = null;

public ?string `$enc_name` = null;

public ?string `$enc_namens` = null;

/\* Методи \*/

public [\_\_construct](soapvar.construct.md)(
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$data`,
?int `$encoding`,
?string `$typeName` = **`null`**,
?string `$typeNamespace` = **`null`**,
?string `$nodeName` = **`null`**,
?string `$nodeNamespace` = **`null`**
)

}

## Властивості

`enc_name`

`enc_namens`

`enc_ns`

`enc_type`

`enc_stype`

`enc_value`

## Зміст

- [SoapVar::\_\_construct](soapvar.construct.md) - Конструктор
SoapVar
