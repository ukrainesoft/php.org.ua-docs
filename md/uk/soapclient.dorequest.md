Виконує SOAP-запит

-   [« SoapClient::construct](soapclient.construct.html)
    
-   [SoapClient::getCookies »](soapclient.getcookies.html)
    
-   [PHP Manual](index.html)
    
-   [SoapClient](class.soapclient.html)
    
-   Виконує SOAP-запит
    

# SoapClient::doRequest

(PHP 5, PHP 7, PHP 8)

SoapClient::doRequest — Виконує запит SOAP

### Опис

```methodsynopsis
public SoapClient::__doRequest(    string $request,    string $location,    string $action,    int $version,    bool $oneWay = false): ?string
```

Виконує SOAP-запит поверх HTTP.

Цей метод може бути перевизначений у підкласах для реалізації інших транспортних рівнів, виконання додаткової обробки XML чи інших цілей.

### Список параметрів

`request`

Запит XML SOAP.

`location`

URL для запиту.

`action`

Дія SOAP.

`version`

Версія SOAP.

`oneWay`

Якщо `oneWay` дорівнює 1, метод нічого не повертає. Цей параметр використовується, коли відповідь не очікується.

### Значення, що повертаються

Відповідь XML SOAP.

### список змін

| Версия | Описание                                                    |
|--------|-------------------------------------------------------------|
|        | Тип `oneWay` тепер bool; раніше він був цілим числом (int). |

### Приклади

**Приклад #1 Приклад використання **SoapClient::doRequest()****

```php
<?php
function Add($x,$y) {
  return $x+$y;
}

class LocalSoapClient extends SoapClient {

  function __construct($wsdl, $options) {
    parent::__construct($wsdl, $options);
    $this->server = new SoapServer($wsdl, $options);
    $this->server->addFunction('Add');
  }

  function __doRequest($request, $location, $action, $version, $one_way = 0) {
    ob_start();
    $this->server->handle($request);
    $response = ob_get_contents();
    ob_end_clean();
    return $response;
  }

}

$x = new LocalSoapClient(NULL,array('location'=>'test://',
                                   'uri'=>'http://testuri.org'));
var_dump($x->Add(3,4));
?>
```