---
navigation:
  - class.soapfault.md: « SoapFault
  - soapfault.tostring.md: 'SoapFault::toString »'
  - index.md: PHP Manual
  - class.soapfault.md: SoapFault
title: 'SoapFault::construct'
---
# SoapFault::construct

(PHP 5, PHP 7, PHP 8)

SoapFault::construct - Конструктор SoapFault

### Опис

public **SoapFault::construct**  
array|string|null `$code`  
string `$string`  
?string `$actor` **`null`**  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$details` **`null`**  
?string `$name` **`null`**  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$headerFault` **`null`**

Цей клас служить для надсилання відповіді на помилку SOAP з обробника PHP . `faultcode` `faultstring` `faultactor` і `detail` є стандартними елементами SOAP.

### Список параметрів

`faultcode`

Код помилки [SoapFault](class.soapfault.md)

`faultstring`

Повідомлення про помилку [SoapFault](class.soapfault.md)

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
function test($x)
{
    return new SoapFault("Server", "Сообщение об ошибке");
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

Можна використовувати механізм виключення PHP для повідомлення про помилки SOAP.

**Приклад #2 Кілька прикладів**

```php
<?php
function test($x)
{
    throw new SoapFault("Server", "Some error message");
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

### Дивіться також

-   [SoapServer::fault()](soapserver.fault.md) - змушує SoapServer повернути помилку
-   [ісsoapfault()](function.is-soap-fault.html) - Перевіряє, чи сталася помилка під час виклику SOAP
