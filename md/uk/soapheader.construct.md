---
navigation:
  - class.soapheader.md: « SoapHeader
  - class.soapparam.md: SoapParam »
  - index.md: PHP Manual
  - class.soapheader.md: SoapHeader
title: 'SoapHeader::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapHeader::\_\_construct

(PHP 5, PHP 7, PHP 8)

SoapHeader::\_\_construct - Конструктор SoapHeader

### Опис

public **SoapHeader::\_\_construct**  
string`$namespace`,  
string`$name`,  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$data`  
bool`$mustunderstand`  
string`$actor`  
) .

Створює новий об'єкт SoapHeader.

### Список параметрів

`namespace`

Простір імен для елемента заголовка SOAP.

`name`

Ім'я об'єкта SoapHeader.

`data`

Вміст заголовка SOAP. Можливо як значенням PHP, і об'єктом [SoapVar](class.soapvar.md)

`mustUnderstand`

Значение атрибута`mustUnderstand` елемент SOAP заголовка.

`actor`

Значение атрибута`actor` елемент SOAP заголовка.

### Приклади

**Приклад #1 Приклад використання** SoapHeader::SoapHeader()\*\*\*\*

```php
<?php
$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$client->__soapCall("echoVoid", null, null,
                new SoapHeader('http://soapinterop.org/echoheader/',
                               'echoMeStringRequest',
                               'hello world'));
?>
```

### Дивіться також

-   [SoapClient::\_\_soapCall()](soapclient.soapcall.md) \- Викликає SOAP-функцію
-   **SoapVar::SoapVar()**
-   **SoapParam::SoapParam()**
-   [SoapServer::addSoapHeader()](soapserver.addsoapheader.md) \- Додати заголовок SOAP у відповідь
