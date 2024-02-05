---
navigation:
  - class.soapparam.md: « SoapParam
  - class.soapvar.md: SoapVar »
  - index.md: PHP Manual
  - class.soapparam.md: SoapParam
title: 'SoapParam::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapParam::\_\_construct

(PHP 5, PHP 7, PHP 8)

SoapParam::\_\_construct - Конструктор SoapParam

### Опис

public**SoapParam::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `$data`, string`$name`) .

Створює новий об'єкт [SoapParam](class.soapparam.md)

### Список параметрів

`data`

Дані передачі або повернення. Цей параметр може передаватися безпосередньо як значення PHP, але в цьому випадку він називатиметься `paramN`, і служба SOAP може його не зрозуміти.

`name`

Назва параметра.

### Приклади

**Пример #1 Пример использования**SoapParam::SoapParam()\*\*\*\*

```php
<?php
$client = new SoapClient(null,array('location' => "http://localhost/soap.php",
                                    'uri'      => "http://test-uri/"));
$client->SomeFunction(new SoapParam($a, "a"),
                      new SoapParam($b, "b"),
                      new SoapParam($c, "c"));
?>
```

### Дивіться також

-   [SoapClient::\_\_soapCall()](soapclient.soapcall.md) \- Викликає SOAP-функцію
-   **SoapVar::SoapVar()**
