Повертає останню SOAP-відповідь

-   [« SoapClient::getLastRequestHeaders](soapclient.getlastrequestheaders.md)
    
-   [SoapClient::getLastResponseHeaders »](soapclient.getlastresponseheaders.md)
    
-   [PHP Manual](index.md)
    
-   [SoapClient](class.soapclient.md)
    
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
> Метод працює лише для об'єкта [SoapClient](class.soapclient.md), створеного з налаштуванням `trace`, рівною **`true`**

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

-   [SoapClient::getLastResponseHeaders()](soapclient.getlastresponseheaders.md) - Повертає SOAP-заголовки останньої відповіді
-   [SoapClient::getLastRequest()](soapclient.getlastrequest.md) - Повертає останній SOAP-запит
-   [SoapClient::getLastRequestHeaders()](soapclient.getlastrequestheaders.md) - Повертає SOAP-заголовки останнього запиту