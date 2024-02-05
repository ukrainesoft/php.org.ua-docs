---
navigation:
  - soapclient.setsoapheaders.md: '« SoapClient::\_\_setSoapHeaders'
  - class.soapserver.md: SoapServer »
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_soapCall'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_soapCall

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_soapCall — Викликає SOAP-функцію

### Опис

```methodsynopsis
public SoapClient::__soapCall(    string $name,    array $args,    ?array $options = null,    SoapHeader|array|null $inputHeaders = null,    array &$outputHeaders = null): mixed
```

Це низькорівнева функція API, яка дозволяє зробити SOAP-дзвінок. Зазвичай у режимі WSDL функції SOAP викликаються як методи об'єкта [SoapClient](class.soapclient.md). Цей метод корисний у режимі, відмінному від WSDL, коли `soapaction`неизвестен,`uri` відрізняється від URI за замовчуванням або під час відправлення та/або отримання SOAP-заголовків.

У разі виникнення помилки виклик SOAP-функції може призвести до виключення або повернення об'єкта [SoapFault](class.soapfault.md), якщо виключення вимкнено. Щоб перевірити, чи виклик функції завершився невдачею, зловивши виняток SoapFault, перевірте результат за допомогою [is\_soap\_fault()](function.is-soap-fault.md)

### Список параметрів

`name`

Ім'я SOAP-функції.

`args`

Масив аргументів, що передаються у функцію. Це може бути впорядкований чи асоціативний масив. Зверніть увагу, що більшість SOAP-серверів вимагають надавати імена параметрів, і в цьому випадку це має бути асоціативний масив.

`options`

Асоціативний масив налаштувань, що передаються клієнту.

Настройка`location` - URL віддаленої веб-служби.

Настройка`uri` - Цільовий простір імен SOAP-служби.

Настройка`soapaction` - Дія для виклику.

`inputHeaders`

Масив заголовків, що надсилаються разом із SOAP-запитом.

`outputHeaders`

Якщо вказано, цей масив буде заповнений заголовками з SOAP-відповіді.

### Значення, що повертаються

Функції SOAP можуть повертати одне чи кілька значень. Якщо функція SOAP повертає лише одне значення, то значення, що повертається, буде скаляром. Якщо повертається кілька значень, замість них повертається асоціативний масив іменованих вихідних параметрів.

У разі виникнення помилки, якщо об'єкт [SoapClient](class.soapclient.md) був оголошений з опцією `exceptions`со значением\*\*`false`\*\*, буде повернуто об'єкт [SoapFault](class.soapfault.md)

### Приклади

**Приклад #1 Приклад використання** SoapClient::\_\_soapCall()\*\*\*\*

```php
<?php

$client = new SoapClient("some.wsdl");
$client->SomeFunction($a, $b, $c);

$client->__soapCall("SomeFunction", array($a, $b, $c));
$client->__soapCall("SomeFunction", array($a, $b, $c), NULL,
                    new SoapHeader(), $output_headers);


$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$client->SomeFunction($a, $b, $c);
$client->__soapCall("SomeFunction", array($a, $b, $c));
$client->__soapCall("SomeFunction", array($a, $b, $c),
                    array('soapaction' => 'some_action',
                          'uri'        => 'some_uri'));
?>
```

### Дивіться також

-   [SoapClient::\_\_construct()](soapclient.construct.md) \- Конструктор класу SoapClient
-   [SoapParam::\_\_construct()](soapparam.construct.md) \- Конструктор SoapParam
-   [SoapVar::\_\_construct()](soapvar.construct.md) \- Конструктор SoapVar
-   [SoapHeader::\_\_construct()](soapheader.construct.md) \- Конструктор SoapHeader
-   [SoapFault::\_\_construct()](soapfault.construct.md) \- Конструктор SoapFault
-   [is\_soap\_fault()](function.is-soap-fault.md) \- Перевіряє, чи сталася помилка під час виклику SOAP
