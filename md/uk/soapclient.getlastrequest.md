Повертає останній SOAP-запит

-   [« SoapClient::\_\_getFunctions](soapclient.getfunctions.html)
    
-   [SoapClient::\_\_getLastRequestHeaders »](soapclient.getlastrequestheaders.html)
    
-   [PHP Manual](index.html)
    
-   [SoapClient](class.soapclient.html)
    
-   Повертає останній SOAP-запит
    

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
> Метод працює лише для об'єкта [SoapClient](class.soapclient.html), створеного з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній запит SOAP у вигляді рядка з XML.

### Приклади

**Приклад #1 Приклад використання SoapClient::getLastRequest()**

```php
<?php
$client = new SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "ЗАПРОС:\n" . $client->__getLastRequest() . "\n";
?>
```

### Дивіться також

-   [SoapClient::\_\_getLastRequestHeaders()](soapclient.getlastrequestheaders.html) - Повертає SOAP-заголовки останнього запиту
-   [SoapClient::\_\_getLastResponse()](soapclient.getlastresponse.html) - Повертає останню SOAP-відповідь
-   [SoapClient::\_\_getLastResponseHeaders()](soapclient.getlastresponseheaders.html) - Повертає SOAP-заголовки останньої відповіді