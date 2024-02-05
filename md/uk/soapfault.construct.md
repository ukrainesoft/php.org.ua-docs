---
navigation:
  - class.soapfault.md: « SoapFault
  - soapfault.tostring.md: 'SoapFault::\_\_toString »'
  - index.md: PHP Manual
  - class.soapfault.md: SoapFault
title: 'SoapFault::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapFault::\_\_construct

(PHP 5, PHP 7, PHP 8)

SoapFault::\_\_construct - Конструктор SoapFault

### Опис

public**SoapFault::\_\_construct**  
array|string|null`$code`,  
string`$string`,  
?string`$actor` **`null`**,  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$details` **`null`**,  
?string`$name` **`null`**,  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$headerFault` **`null`**  
) .

Цей клас служить для надсилання відповіді на помилку SOAP з обробника PHP . `faultcode` `faultstring` `faultactor`и`detail` є стандартними елементами SOAP.

### Список параметрів

`faultcode`

Код ошибки[SoapFault](class.soapfault.md)

`faultstring`

Сообщение об ошибке[SoapFault](class.soapfault.md)

`faultactor`

Рядок ідентифікує відправника, що спричинив помилку.

`detail`

Детальна інформація щодо причин помилки.

`faultname`

Може бути використаний для вибору коректного кодування помилки з WSDL.

`headerfault`

Може бути використане під час обробки заголовка SOAP для повідомлення про помилку у заголовку відповіді.

### Приклади

**Приклад #1 Кілька прикладів**

```php
<?php
function test($x)
{
    return new SoapFault("Server", "Сообщение об ошибке");
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

Можна використовувати механізм виключення PHP для повідомлення про помилки SOAP.

**Приклад #2 Кілька прикладів**

```php
<?php
function test($x)
{
    throw new SoapFault("Server", "Some error message");
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

### Дивіться також

-   [SoapServer::fault()](soapserver.fault.md) \- змушує SoapServer повернути помилку
-   [is\_soap\_fault()](function.is-soap-fault.md) \- Перевіряє, чи сталася помилка під час виклику SOAP
