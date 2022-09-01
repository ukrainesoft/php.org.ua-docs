---
navigation:
  - soapclient.setsoapheaders.md: '« SoapClient::setSoapHeaders'
  - class.soapserver.md: SoapServer »
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::soapCall'
---
# SoapClient::soapCall

(PHP 5, PHP 7, PHP 8)

SoapClient::soapCall — Викликає SOAP-функцію

### Опис

```methodsynopsis
public SoapClient::__soapCall(    string $name,    array $args,    ?array $options = null,    SoapHeader|array|null $inputHeaders = null,    array &$outputHeaders = null): mixed
```

Це низькорівнева функція API, яка дозволяє зробити SOAP-дзвінок. Зазвичай у режимі WSDL функції SOAP викликаються як методи об'єкта [SoapClient](class.soapclient.md). Цей метод корисний у режимі, відмінному від WSDL, коли `soapaction` невідомий, `uri` відрізняється від URI за замовчуванням або під час відправлення та/або отримання SOAP-заголовків.

У разі виникнення помилки виклик SOAP-функції може призвести до виключення або повернення об'єкта [SoapFault](class.soapfault.md), якщо виключення вимкнено. Щоб перевірити, чи виклик функції завершився невдачею, зловивши виняток SoapFault, перевірте результат за допомогою [ісsoapfault()](function.is-soap-fault.html)

### Список параметрів

`name`

Ім'я SOAP-функції.

`args`

Масив аргументів, що передаються у функцію. Це може бути впорядкований чи асоціативний масив. Зверніть увагу, що більшість SOAP-серверів вимагають надавати імена параметрів, і в цьому випадку це має бути асоціативний масив.

`options`

Асоціативний масив налаштувань, що передаються клієнту.

Налаштування `location` - URL віддаленої веб-служби.

Налаштування `uri` - Цільовий простір імен SOAP-служби.

Налаштування `soapaction` - Дія для виклику.

`inputHeaders`

Масив заголовків, що надсилаються разом із SOAP-запитом.

`outputHeaders`

Якщо вказано, цей масив буде заповнений заголовками з SOAP-відповіді.

### Значення, що повертаються

Функції SOAP можуть повертати одне чи кілька значень. Якщо функція SOAP повертає лише одне значення, то значення, що повертається, буде скаляром. Якщо повертається кілька значень, замість них повертається асоціативний масив іменованих вихідних параметрів.

У разі виникнення помилки, якщо об'єкт [SoapClient](class.soapclient.md) був оголошений з опцією `exceptions` зі значенням **`false`**, буде повернуто об'єкт [SoapFault](class.soapfault.md)

### Приклади

**Приклад #1 Приклад використання **SoapClient::soapCall()****

```php
<?php

$client = new SoapClient("some.wsdl");
$client->SomeFunction($a, $b, $c);

$client->__soapCall("SomeFunction", array($a, $b, $c));
$client->__soapCall("SomeFunction", array($a, $b, $c), NULL,
                    new SoapHeader(), $output_headers);


$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$client->SomeFunction($a, $b, $c);
$client->__soapCall("SomeFunction", array($a, $b, $c));
$client->__soapCall("SomeFunction", array($a, $b, $c),
                    array('soapaction' => 'some_action',
                          'uri'        => 'some_uri'));
?>
```

### Дивіться також

-   [SoapClient::construct()](soapclient.construct.md) - Конструктор класу SoapClient
-   [SoapParam::construct()](soapparam.construct.md) - Конструктор SoapParam
-   [SoapVar::construct()](soapvar.construct.md) - Конструктор SoapVar
-   [SoapHeader::construct()](soapheader.construct.md) - Конструктор SoapHeader
-   [SoapFault::construct()](soapfault.construct.md) - Конструктор SoapFault
-   [ісsoapfault()](function.is-soap-fault.html) - Перевіряє, чи сталася помилка під час виклику SOAP
