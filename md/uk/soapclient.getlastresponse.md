Повертає останню SOAP-відповідь

-   [« SoapClient::\_\_getLastRequestHeaders](soapclient.getlastrequestheaders.html)
    
-   [SoapClient::\_\_getLastResponseHeaders »](soapclient.getlastresponseheaders.html)
    
-   [PHP Manual](index.html)
    
-   [SoapClient](class.soapclient.html)
    
-   Повертає останню SOAP-відповідь
    

# SoapClient::getLastResponse

(PHP 5, PHP 7, PHP 8)

SoapClient::getLastResponse — Повертає останню SOAP-відповідь

### Опис

```methodsynopsis
public SoapClient::__getLastResponse(): ?string
```

Повертає XML, отриманий в останній SOAP-відповіді.

> **Зауваження**
> 
> Метод працює лише для об'єкта [SoapClient](class.soapclient.html), створеного з налаштуванням `trace`, рівною **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Остання відповідь SOAP у вигляді рядка з XML.

### Приклади

**Приклад #1 Приклад використання SoapClient::getLastResponse()**

```php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "Ответ:\n" . $client->__getLastResponse() . "\n";
?>
```

### Дивіться також

-   [SoapClient::\_\_getLastResponseHeaders()](soapclient.getlastresponseheaders.html) - Повертає SOAP-заголовки останньої відповіді
-   [SoapClient::\_\_getLastRequest()](soapclient.getlastrequest.html) - Повертає останній SOAP-запит
-   [SoapClient::\_\_getLastRequestHeaders()](soapclient.getlastrequestheaders.html) - Повертає SOAP-заголовки останнього запиту