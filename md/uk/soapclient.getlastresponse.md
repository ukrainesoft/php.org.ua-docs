---
navigation:
  - soapclient.getlastrequestheaders.md: '« SoapClient::\_\_getLastRequestHeaders'
  - soapclient.getlastresponseheaders.md: 'SoapClient::\_\_getLastResponseHeaders »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_getLastResponse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_getLastResponse

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_getLastResponse — Повертає останню SOAP-відповідь

### Опис

```methodsynopsis
public SoapClient::__getLastResponse(): ?string
```

Повертає XML, отриманий в останній SOAP-відповіді.

> **Зауваження** :
> 
> Метод працює лише для об'єкта [SoapClient](class.soapclient.md), створеного з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Остання відповідь SOAP у вигляді рядка з XML.

### Приклади

**Приклад #1 Приклад використання SoapClient::\_\_getLastResponse()**

```php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "Ответ:\n" . $client->__getLastResponse() . "\n";
?>
```

### Дивіться також

-   [SoapClient::\_\_getLastResponseHeaders()](soapclient.getlastresponseheaders.md) \- Повертає SOAP-заголовки останньої відповіді
-   [SoapClient::\_\_getLastRequest()](soapclient.getlastrequest.md) \- Повертає останній SOAP-запит
-   [SoapClient::\_\_getLastRequestHeaders()](soapclient.getlastrequestheaders.md) \- Повертає SOAP-заголовки останнього запиту
