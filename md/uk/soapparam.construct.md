---
navigation:
  - class.soapparam.md: « SoapParam
  - class.soapvar.md: SoapVar »
  - index.md: PHP Manual
  - class.soapparam.md: SoapParam
title: 'SoapParam::construct'
---
# SoapParam::construct

(PHP 5, PHP 7, PHP 8)

SoapParam::construct - Конструктор SoapParam

### Опис

public **SoapParam::construct**[mixed](language.types.declarations.md#language.types.declarations.mixed) `$data`, string `$name`

Створює новий об'єкт [SoapParam](class.soapparam.md)

### Список параметрів

`data`

Дані передачі або повернення. Цей параметр може передаватися безпосередньо як значення PHP, але в цьому випадку він називатиметься `paramN`, і служба SOAP може його не зрозуміти.

`name`

Назва параметра.

### Приклади

**Приклад #1 Приклад використання **SoapParam::SoapParam()****

```php
<?php
$client = new SoapClient(null,array('location' => "http://localhost/soap.php",
                                    'uri'      => "http://test-uri/"));
$client->SomeFunction(new SoapParam($a, "a"),
                      new SoapParam($b, "b"),
                      new SoapParam($c, "c"));
?>
```

### Дивіться також

-   [SoapClient::soapCall()](soapclient.soapcall.md) - Викликає SOAP-функцію
-   **SoapVar::SoapVar()**
