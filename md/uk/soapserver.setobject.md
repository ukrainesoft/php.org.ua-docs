Встановлює об'єкт, який використовуватиметься для обробки SOAP-запитів

-   [« SoapServer::setClass](soapserver.setclass.html)
    
-   [SoapServer::setPersistence »](soapserver.setpersistence.html)
    
-   [PHP Manual](index.html)
    
-   [SoapServer](class.soapserver.html)
    
-   Встановлює об'єкт, який використовуватиметься для обробки SOAP-запитів
    

# SoapServer::setObject

(PHP 5> = 5.2.0, PHP 7, PHP 8)

SoapServer::setObject — Встановлює об'єкт, який використовуватиметься для обробки SOAP-запитів

### Опис

```methodsynopsis
public SoapServer::setObject(object $object): void
```

Встановлює об'єкт, який буде використовуватися для обробки SOAP-запитів, а не тільки клас, як у [SoapServer::setClass()](soapserver.setclass.html)

### Список параметрів

`object`

Об'єкт обробки запитів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [SoapServer::setClass()](soapserver.setclass.html) - Встановлює клас, який обробляє SOAP-запити