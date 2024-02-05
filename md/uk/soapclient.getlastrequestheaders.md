---
navigation:
  - soapclient.getlastrequest.md: '« SoapClient::\_\_getLastRequest'
  - soapclient.getlastresponse.md: 'SoapClient::\_\_getLastResponse »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_getLastRequestHeaders'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_getLastRequestHeaders

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_getLastRequestHeaders — Повертає SOAP-заголовки останнього запиту

### Опис

```methodsynopsis
public SoapClient::__getLastRequestHeaders(): ?string
```

Повертає SOAP заголовки останнього запиту.

> **Зауваження** :
> 
> Функція працює лише, якщо об'єкт [SoapClient](class.soapclient.md) був створений з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Заголовки останнього SOAP-запиту.

### Приклади

**Приклад #1 Приклад використання SoapClient::\_\_getLastRequestHeaders()**

```php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "ЗАГОЛОВКИ ЗАПРОСА:\n" . $client->__getLastRequestHeaders() . "\n";
?>
```

### Дивіться також

-   [SoapClient::\_\_getLastResponseHeaders()](soapclient.getlastresponseheaders.md) \- Повертає SOAP-заголовки останньої відповіді
-   [SoapClient::\_\_getLastRequest()](soapclient.getlastrequest.md) \- Повертає останній SOAP-запит
-   [SoapClient::\_\_getLastResponse()](soapclient.getlastresponse.md) \- Повертає останню SOAP-відповідь
