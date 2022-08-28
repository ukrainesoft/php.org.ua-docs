Повертає SOAP-заголовки останньої відповіді

-   [« SoapClient::\_\_getLastResponse](soapclient.getlastresponse.html)
    
-   [SoapClient::\_\_getTypes »](soapclient.gettypes.html)
    
-   [PHP Manual](index.html)
    
-   [SoapClient](class.soapclient.html)
    
-   Повертає SOAP-заголовки останньої відповіді
    

# SoapClient::getLastResponseHeaders

(PHP 5, PHP 7, PHP 8)

SoapClient::getLastResponseHeaders — Повертає SOAP-заголовки останньої відповіді

### Опис

```methodsynopsis
public SoapClient::__getLastResponseHeaders(): ?string
```

Повертає SOAP-заголовки останньої відповіді.

> **Зауваження**
> 
> Функція працює лише, якщо об'єкт [SoapClient](class.soapclient.html) був створений з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Заголовки останньої SOAP-відповіді.

### Приклади

**Приклад #1 Приклад використання SoapClient::getLastResponse()**

```php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "ЗАГОЛОВКИ ОТВЕТА:\n" . $client->__getLastResponseHeaders() . "\n";
?>
```

### Дивіться також

-   [SoapClient::\_\_getLastRequestHeaders()](soapclient.getlastrequestheaders.html) - Повертає SOAP-заголовки останнього запиту
-   [SoapClient::\_\_getLastRequest()](soapclient.getlastrequest.html) - Повертає останній SOAP-запит
-   [SoapClient::\_\_getLastResponse()](soapclient.getlastresponse.html) - Повертає останню SOAP-відповідь