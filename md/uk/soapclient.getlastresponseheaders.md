---
navigation:
  - soapclient.getlastresponse.md: '« SoapClient::\_\_getLastResponse'
  - soapclient.gettypes.md: 'SoapClient::\_\_getTypes »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_getLastResponseHeaders'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_getLastResponseHeaders

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_getLastResponseHeaders — Повертає SOAP-заголовки останньої відповіді

### Опис

```methodsynopsis
public SoapClient::__getLastResponseHeaders(): ?string
```

Повертає SOAP-заголовки останньої відповіді.

> **Зауваження** :
> 
> Функція працює лише, якщо об'єкт [SoapClient](class.soapclient.md) був створений з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Заголовки останньої SOAP-відповіді.

### Приклади

**Приклад #1 Приклад використання SoapClient::\_\_getLastResponse()**

```php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "ЗАГОЛОВКИ ОТВЕТА:\n" . $client->__getLastResponseHeaders() . "\n";
?>
```

### Дивіться також

-   [SoapClient::\_\_getLastRequestHeaders()](soapclient.getlastrequestheaders.md) \- Повертає SOAP-заголовки останнього запиту
-   [SoapClient::\_\_getLastRequest()](soapclient.getlastrequest.md) \- Повертає останній SOAP-запит
-   [SoapClient::\_\_getLastResponse()](soapclient.getlastresponse.md) \- Повертає останню SOAP-відповідь
