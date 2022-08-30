Додає одну або кілька функцій для обробки запитів SOAP

-   [« SoapServer](class.soapserver.html)
    
-   [SoapServer::addSoapHeader »](soapserver.addsoapheader.html)
    
-   [PHP Manual](index.html)
    
-   [SoapServer](class.soapserver.html)
    
-   Додає одну або кілька функцій для обробки запитів SOAP
    

# SoapServer::addFunction

(PHP 5, PHP 7, PHP 8)

SoapServer::addFunction — Додає одну або кілька функцій для обробки запитів SOAP

### Опис

```methodsynopsis
public SoapServer::addFunction(array|string|int $functions): void
```

Експортує одну або кілька функцій віддаленому клієнту

### Список параметрів

`functions`

Для експорту однієї функції передайте в цей параметр її ім'я у вигляді рядка.

Для експорту кількох функцій передайте в цей параметр масив з іменами функцій.

Для експорту всіх функцій задайте параметр константою **`SOAP_FUNCTIONS_ALL`**

> **Зауваження**
> 
> Параметр `functions` повинен приймати всі вхідні аргументи в тому ж порядку, як вони визначені у файлі WSDL (вони не повинні приймати жодних параметрів, що повертаються в якості аргументів) і повинні повертати одне або більше значень. Для повернення кількох значень, вони повинні повертати масив з іменованими параметрами, що повертаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SoapServer::addFunction()****

```php
<?php

function echoString($inputString)
{
    return $inputString;
}

$server->addFunction("echoString");

function echoTwoStrings($inputString1, $inputString2)
{
    return array("outputString1" => $inputString1,
                 "outputString2" => $inputString2);
}
$server->addFunction(array("echoString", "echoTwoStrings"));

$server->addFunction(SOAP_FUNCTIONS_ALL);

?>
```

### Дивіться також

-   [SoapServer::construct()](soapserver.construct.html) - Конструктор SoapServer
-   [SoapServer::setClass()](soapserver.setclass.html) - Встановлює клас, який обробляє SOAP-запити