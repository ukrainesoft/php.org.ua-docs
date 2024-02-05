---
navigation:
  - soapclient.construct.md: '« SoapClient::\_\_construct'
  - soapclient.getcookies.md: 'SoapClient::\_\_getCookies »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_doRequest'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_doRequest

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_doRequest — Виконує запит SOAP

### Опис

```methodsynopsis
public SoapClient::__doRequest(    string $request,    string $location,    string $action,    int $version,    bool $oneWay = false): ?string
```

Виконує SOAP-запит поверх HTTP.

Цей метод може бути перевизначений у підкласах реалізації інших транспортних рівнів, виконання додаткової обробки XML чи інших цілей.

### Список параметрів

`request`

Запит XML SOAP.

`location`

URL-адреса для запиту.

`action`

Дія SOAP.

`version`

Версія SOAP.

`oneWay`

Якщо `oneWay`равен\*\*`true`\*\*метод нічого не повертає. Цей параметр використовується, коли відповідь не очікується.

### Значення, що повертаються

Відповідь XML SOAP.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тип`oneWay` тепер bool; раніше він був цілим числом (int). |

### Приклади

**Пример #1 Пример использования**SoapClient::\_\_doRequest()\*\*\*\*

```php
<?php
function Add($x,$y) {
  return $x+$y;
}

class LocalSoapClient extends SoapClient {

  function __construct($wsdl, $options) {
    parent::__construct($wsdl, $options);
    $this->server = new SoapServer($wsdl, $options);
    $this->server->addFunction('Add');
  }

  function __doRequest($request, $location, $action, $version, $one_way = 0) {
    ob_start();
    $this->server->handle($request);
    $response = ob_get_contents();
    ob_end_clean();
    return $response;
  }

}

$x = new LocalSoapClient(NULL,array('location'=>'test://',
                                   'uri'=>'http://testuri.org'));
var_dump($x->Add(3,4));
?>
```
