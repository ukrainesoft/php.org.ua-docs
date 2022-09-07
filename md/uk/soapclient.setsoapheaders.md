---
navigation:
  - soapclient.setlocation.md: '« SoapClient::setLocation'
  - soapclient.soapcall.md: 'SoapClient::soapCall »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::setSoapHeaders'
---
# SoapClient::setSoapHeaders

(PHP 5> = 5.0.5, PHP 7, PHP 8)

SoapClient::setSoapHeaders — Встановлює заголовки SOAP для наступних дзвінків

### Опис

```methodsynopsis
public SoapClient::__setSoapHeaders(SoapHeader|array|null $headers = null): bool
```

Визначає заголовки для надсилання разом із SOAP-запитами.

> **Зауваження**
> 
> Виклик цього методу замінить будь-які попередні значення.

### Список параметрів

`headers`

Заголовки, що встановлюються. Це може бути об'єкт [SoapHeader](class.soapheader.md) або масив об'єктів [SoapHeader](class.soapheader.md). Якщо не вказано чи одно **`null`**, заголовки будуть видалені.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SoapClient::setSoapHeaders()****

```php
<?php

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$header = new SoapHeader('http://soapinterop.org/echoheader/',
                            'echoMeStringRequest',
                            'hello world');

$client->__setSoapHeaders($header);

$client->__soapCall("echoVoid", null);
?>
```

**Приклад #2 Встановлення кількох заголовків**

```php
<?php

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$headers = array();

$headers[] = new SoapHeader('http://soapinterop.org/echoheader/',
                            'echoMeStringRequest',
                            'hello world');

$headers[] = new SoapHeader('http://soapinterop.org/echoheader/',
                            'echoMeStringRequest',
                            'hello world again');

$client->__setSoapHeaders($headers);

$client->__soapCall("echoVoid", null);
?>
```
