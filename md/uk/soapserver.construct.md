Конструктор SoapServer

-   [« SoapServer::addSoapHeader](soapserver.addsoapheader.md)
    
-   [SoapServer::fault »](soapserver.fault.md)
    
-   [PHP Manual](index.md)
    
-   [SoapServer](class.soapserver.md)
    
-   Конструктор SoapServer
    

# SoapServer::construct

(PHP 5, PHP 7, PHP 8)

SoapServer::construct — Конструктор SoapServer

### Опис

public **SoapServer::construct**(?string `$wsdl`, array `$options`

Цей конструктор дозволяє створювати об'єкти [SoapServer](class.soapserver.md) у WSDL чи не-WSDL режимах.

### Список параметрів

`wsdl`

Для використання SoapServer в режимі WSDL вкажіть URI WSDL-файлу. В іншому випадку вкажіть **`null`** та встановіть опцію `uri` рівної простору імен сервера.

`options`

Спроба встановити стандартну версію SOAP (`soap_version`), внутрішнє кодування (`encoding`) та URI відправника (`actor`

Опцію `classmap` можна використовувати для порівняння деяких типів WSDL із класами PHP. Ця опція повинна бути масивом з ключами рівними типу WSDL і значенням рівними іменам класів PHP.

Опція `typemap` є масивом зіставлення типів. Масив із ключами `type_name` `type_ns` (URI простору імен), `from_xml` (callback-функція, що приймає один рядковий параметр) та `to_xml` (callback-функція, що приймає один об'єкт як параметр).

Опція `cache_wsdl` задається однією з констант: **`WSDL_CACHE_NONE`** **`WSDL_CACHE_DISK`** **`WSDL_CACHE_MEMORY`** або **`WSDL_CACHE_BOTH`**

Також є опція `features`, яка задається однією з констант: **`SOAP_WAIT_ONE_WAY_CALLS`** **`SOAP_SINGLE_ELEMENT_ARRAYS`** або **`SOAP_USE_XSI_ARRAY_TYPE`**

опція `send_errors` може бути встановлена ​​в **`false`** для надсилання загального повідомлення про помилку ("Internal error") замість спеціального повідомлення про помилку, яке надсилається в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SoapServer::SoapServer()****

```php
<?php

$server = new SoapServer("some.wsdl");

$server = new SoapServer("some.wsdl", array('soap_version' => SOAP_1_2));

$server = new SoapServer("some.wsdl", array('actor' => "http://example.org/ts-tests/C"));

$server = new SoapServer("some.wsdl", array('encoding'=>'ISO-8859-1'));

$server = new SoapServer(null, array('uri' => "http://test-uri/"));

class MyBook {
    public $title;
    public $author;
}

$server = new SoapServer("books.wsdl", array('classmap' => array('book' => "MyBook")));

?>
```

### Дивіться також

-   **SoapClient::SoapClient()**