---
navigation:
  - class.soapclient.md: « SoapClient
  - soapclient.construct.md: 'SoapClient::\_\_construct »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_call'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_call

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_call - Викликає SOAP-функцію (застарілий метод)

### Опис

```methodsynopsis
public SoapClient::__call(string $name, array $args): mixed
```

Виклик цього методу застарів. Зазвичай функції SOAP можуть бути викликані як методи об'єкта [SoapClient](class.soapclient.md); у ситуаціях, коли це неможливо або потрібні додаткові опції, використовуйте метод [SoapClient::\_\_soapCall()](soapclient.soapcall.md) .. .

### Список параметрів

`name`

Ім'я функції SOAP.

`args`

Масив аргументів передачі функції. Може бути впорядкований чи асоціативний масив. Зверніть увагу, що більшість серверів SOAP вимагають надання імен параметрів, у цьому випадку має бути асоціативний масив.

### Значення, що повертаються

Функції SOAP можуть повертати одне чи кілька значень. Якщо функція SOAP повертає лише одне значення, то значення, що повертається, буде скаляром. Якщо повертається кілька значень, замість них повертається асоціативний масив іменованих вихідних параметрів.

У разі виникнення помилки, якщо об'єкт [SoapClient](class.soapclient.md) був оголошений з опцією `exceptions`со значением\*\*`false`\*\*, буде повернуто об'єкт [SoapFault](class.soapfault.md)
