---
navigation:
  - soapclient.getfunctions.md: '« SoapClient::\_\_getFunctions'
  - soapclient.getlastrequestheaders.md: 'SoapClient::\_\_getLastRequestHeaders »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_getLastRequest'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_getLastRequest

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_getLastRequest - Повертає останній SOAP-запит

### Опис

```methodsynopsis
public SoapClient::__getLastRequest(): ?string
```

Повертає XML, переданий в останньому запиті SOAP.

> **Зауваження** :
> 
> Метод працює лише для об'єкта [SoapClient](class.soapclient.md), створеного з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній запит SOAP у вигляді рядка з XML.

### Приклади

**Приклад #1 Приклад використання SoapClient::\_\_getLastRequest()**

```php
<?php
$client = new SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "ЗАПРОС:\n" . $client->__getLastRequest() . "\n";
?>
```

### Дивіться також

-   [SoapClient::\_\_getLastRequestHeaders()](soapclient.getlastrequestheaders.md) \- Повертає SOAP-заголовки останнього запиту
-   [SoapClient::\_\_getLastResponse()](soapclient.getlastresponse.md) \- Повертає останню SOAP-відповідь
-   [SoapClient::\_\_getLastResponseHeaders()](soapclient.getlastresponseheaders.md) \- Повертає SOAP-заголовки останньої відповіді
