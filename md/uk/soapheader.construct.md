Конструктор SoapHeader

-   [« SoapHeader](class.soapheader.html)
    
-   [SoapParam »](class.soapparam.html)
    
-   [PHP Manual](index.html)
    
-   [SoapHeader](class.soapheader.html)
    
-   Конструктор SoapHeader
    

# SoapHeader::construct

(PHP 5, PHP 7, PHP 8)

SoapHeader::construct - Конструктор SoapHeader

### Опис

**SoapHeader::construct**  
string `$namespace`  
string `$name`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data`  
bool `$mustunderstand`  
string `$actor`  

Створює новий об'єкт SoapHeader.

### Список параметрів

`namespace`

Простір імен для елемента заголовка SOAP.

`name`

Ім'я об'єкта SoapHeader.

`data`

Вміст заголовка SOAP. Можливо як значенням PHP, і об'єктом [SoapVar](class.soapvar.html)

`mustUnderstand`

Значення атрибуту `mustUnderstand` елемент SOAP заголовка.

`actor`

Значення атрибуту `actor` елемент SOAP заголовка.

### Приклади

**Приклад #1 Приклад використання **SoapHeader::SoapHeader()****

```php
<?php
$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$client->__soapCall("echoVoid", null, null,
                new SoapHeader('http://soapinterop.org/echoheader/',
                               'echoMeStringRequest',
                               'hello world'));
?>
```

### Дивіться також

-   [SoapClient::\_\_soapCall()](soapclient.soapcall.html) - Викликає SOAP-функцію
-   **SoapVar::SoapVar()**
-   **SoapParam::SoapParam()**
-   [SoapServer::addSoapHeader()](soapserver.addsoapheader.html) - Додати заголовок SOAP у відповідь