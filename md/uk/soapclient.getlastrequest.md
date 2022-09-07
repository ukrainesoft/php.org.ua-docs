---
navigation:
  - soapclient.getfunctions.md: '« SoapClient::getFunctions'
  - soapclient.getlastrequestheaders.md: 'SoapClient::getLastRequestHeaders »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::getLastRequest'
---
# SoapClient::getLastRequest

(PHP 5, PHP 7, PHP 8)

SoapClient::getLastRequest - Повертає останній SOAP-запит

### Опис

```methodsynopsis
public SoapClient::__getLastRequest(): ?string
```

Повертає XML, переданий в останньому запиті SOAP.

> **Зауваження**
> 
> Метод працює лише для об'єкта [SoapClient](class.soapclient.md), створеного з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній запит SOAP у вигляді рядка з XML.

### Приклади

**Приклад #1 Приклад використання SoapClient::getLastRequest()**

```php
<?php
$client = new SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "ЗАПРОС:\n" . $client->__getLastRequest() . "\n";
?>
```

### Дивіться також

-   [SoapClient::getLastRequestHeaders()](soapclient.getlastrequestheaders.md) - Повертає SOAP-заголовки останнього запиту
-   [SoapClient::getLastResponse()](soapclient.getlastresponse.md) - Повертає останню SOAP-відповідь
-   [SoapClient::getLastResponseHeaders()](soapclient.getlastresponseheaders.md) - Повертає SOAP-заголовки останньої відповіді
