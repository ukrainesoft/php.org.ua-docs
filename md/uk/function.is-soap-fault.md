Перевіряє, чи сталася помилка під час виклику SOAP

-   [« Функции SOAP](ref.soap.html)
    
-   [usesoaperrorhandler »](function.use-soap-error-handler.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SOAP](ref.soap.html)
    
-   Перевіряє, чи сталася помилка під час виклику SOAP
    

# ісsoapfault

(PHP 5, PHP 7, PHP 8)

ісsoapfault — Перевіряє, чи виникла помилка під час виклику SOAP

### Опис

```methodsynopsis
is_soap_fault(mixed $object): bool
```

Ця функція корисна для перевірки невдачі виклику SOAP, але тоді, коли не використовуються винятки. Для того щоб її використовувати, створіть об'єкт [SoapClient](class.soapclient.html) з опцією `exceptions`, що дорівнює нулю або **`false`**. У цьому випадку метод SOAP поверне спеціальний об'єкт [SoapFault](class.soapfault.html), який інкапсулює деталі помилки (код помилки, рядок помилки, одержувач та деталі).

Якщо опція `exceptions` не встановлено, то виклик SOAP буде викидати виняток у разі виникнення помилки. Функція **ісsoapfault()** перевіряє, чи є переданий параметр об'єктом [SoapFault](class.soapfault.html)

### Список параметрів

`object`

Об'єкт перевірки.

### Значення, що повертаються

Повертається **`true`** у разі виникнення помилки та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання функції **ісsoapfault()****

```php
<?php
$client = new SoapClient("some.wsdl", array('exceptions' => 0));
$result = $client->SomeFunction();
if (is_soap_fault($result)) {
    trigger_error("Ошибка SOAP: (faultcode: {$result->faultcode}, faultstring: {$result->faultstring})", E_USER_ERROR);
}
?>
```

**Приклад #2 Стандартний метод SOAP для повідомлень про помилки - це винятки**

```php
<?php
try {
    $client = new SoapClient("some.wsdl");
    $result = $client->SomeFunction(/* ... */);
} catch (SoapFault $fault) {
    trigger_error("Ошибка SOAP: (faultcode: {$fault->faultcode}, faultstring: {$fault->faultstring})", E_USER_ERROR);
}
?>
```

### Дивіться також

-   [SoapClient::construct()](soapclient.construct.html) - Конструктор класу SoapClient
-   [SoapFault::construct()](soapfault.construct.html) - Конструктор SoapFault