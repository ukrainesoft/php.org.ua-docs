Встановлює адресу веб-служби, що використовується

-   [« SoapClient::\_\_setCookie](soapclient.setcookie.html)
    
-   [SoapClient::\_\_setSoapHeaders »](soapclient.setsoapheaders.html)
    
-   [PHP Manual](index.html)
    
-   [SoapClient](class.soapclient.html)
    
-   Встановлює адресу веб-служби, що використовується
    

# SoapClient::setLocation

(PHP 5> = 5.0.4, PHP 7, PHP 8)

SoapClient::setLocation — Встановлює адресу веб-служби, що використовується.

### Опис

```methodsynopsis
public SoapClient::__setLocation(?string $location = null): ?string
```

Встановлює URL кінцевої точки, що стосується наступних SOAP-запитів. Еквівалентна налаштуванню `location`, що вказується в конструкторі SoapClient.

> **Зауваження**
> 
> Виклик методу необов'язковий. За замовчуванням SoapClient використовує адресу з файлу WSDL.

### Список параметрів

`location`

Новий URL кінцевої точки.

### Значення, що повертаються

Старий URL кінцевої точки.

### список змін

| Версия | Описание                                 |
|--------|------------------------------------------|
|        | `location` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **SoapClient::setLocation()****

```php
<?php
$client = new SoapClient('http://example.com/webservice.php?wsdl');

$client->__setLocation('http://www.somethirdparty.com');

$old_location = $client->__setLocation(); // сбрасывает настройку адреса

echo $old_location;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
http://www.somethirdparty.com
```

### Дивіться також

-   [SoapClient::\_\_construct()](soapclient.construct.html) - Конструктор класу SoapClient