---
navigation:
  - ref.soap.md: « Функції SOAP
  - function.use-soap-error-handler.md: use\_soap\_error\_handler »
  - index.md: PHP Manual
  - ref.soap.md: Функції SOAP
title: is\_soap\_fault
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_soap\_fault

(PHP 5, PHP 7, PHP 8)

is\_soap\_fault — Перевіряє, чи виникла помилка під час виклику SOAP

### Опис

```methodsynopsis
is_soap_fault(mixed $object): bool
```

Ця функція корисна для перевірки невдачі виклику SOAP, але тоді, коли не використовуються винятки. Для того щоб її використовувати, створіть об'єкт [SoapClient](class.soapclient.md) з опцією `exceptions`, що дорівнює нулю або **`false`**. У цьому випадку метод SOAP поверне спеціальний об'єкт [SoapFault](class.soapfault.md), який інкапсулює деталі помилки (код помилки, рядок помилки, одержувач та деталі).

Якщо опція `exceptions` не встановлено, то виклик SOAP буде викидати виняток у разі виникнення помилки. Функція **is\_soap\_fault()** перевіряє, чи є переданий параметр об'єктом [SoapFault](class.soapfault.md)

### Список параметрів

`object`

Об'єкт перевірки.

### Значення, що повертаються

Повертається **`true`**в случае возникновения ошибки и**`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад использования функции**is\_soap\_fault()\*\*\*\*

```php
<?php
$client = new SoapClient("some.wsdl", array('exceptions' => 0));
$result = $client->SomeFunction();
if (is_soap_fault($result)) {
    trigger_error("Ошибка SOAP: (faultcode: {$result->faultcode}, faultstring: {$result->faultstring})", E_USER_ERROR);
}
?>
```

**Приклад #2 Стандартний метод SOAP для повідомлень про помилки - це винятки**

```php
<?php
try {
    $client = new SoapClient("some.wsdl");
    $result = $client->SomeFunction(/* ... */);
} catch (SoapFault $fault) {
    trigger_error("Ошибка SOAP: (faultcode: {$fault->faultcode}, faultstring: {$fault->faultstring})", E_USER_ERROR);
}
?>
```

### Дивіться також

-   [SoapClient::\_\_construct()](soapclient.construct.md) \- Конструктор класу SoapClient
-   [SoapFault::\_\_construct()](soapfault.construct.md) \- Конструктор SoapFault
