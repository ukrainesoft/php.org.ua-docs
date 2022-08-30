Повертає SOAP-заголовки останнього запиту

-   [« SoapClient::getLastRequest](soapclient.getlastrequest.html)
    
-   [SoapClient::getLastResponse »](soapclient.getlastresponse.html)
    
-   [PHP Manual](index.html)
    
-   [SoapClient](class.soapclient.html)
    
-   Повертає SOAP-заголовки останнього запиту
    

# SoapClient::getLastRequestHeaders

(PHP 5, PHP 7, PHP 8)

SoapClient::getLastRequestHeaders — Повертає SOAP-заголовки останнього запиту

### Опис

```methodsynopsis
public SoapClient::__getLastRequestHeaders(): ?string
```

Повертає SOAP заголовки останнього запиту.

> **Зауваження**
> 
> Функція працює лише, якщо об'єкт [SoapClient](class.soapclient.html) був створений з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Заголовки останнього SOAP-запиту.

### Приклади

**Приклад #1 Приклад використання SoapClient::getLastRequestHeaders()**

```php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "ЗАГОЛОВКИ ЗАПРОСА:\n" . $client->__getLastRequestHeaders() . "\n";
?>
```

### Дивіться також

-   [SoapClient::getLastResponseHeaders()](soapclient.getlastresponseheaders.html) - Повертає SOAP-заголовки останньої відповіді
-   [SoapClient::getLastRequest()](soapclient.getlastrequest.html) - Повертає останній SOAP-запит
-   [SoapClient::getLastResponse()](soapclient.getlastresponse.html) - Повертає останню SOAP-відповідь