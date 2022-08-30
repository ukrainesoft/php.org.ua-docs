Обробка SOAP-запиту

-   [« SoapServer::getFunctions](soapserver.getfunctions.md)
    
-   [SoapServer::setClass »](soapserver.setclass.md)
    
-   [PHP Manual](index.md)
    
-   [SoapServer](class.soapserver.md)
    
-   Обробка SOAP-запиту
    

# SoapServer::handle

(PHP 5, PHP 7, PHP 8)

SoapServer::handle — Обробка SOAP-запиту

### Опис

```methodsynopsis
public SoapServer::handle(?string $request = null): void
```

Обробляє SOAP-запит, викликає необхідні функції та надсилає відповідь клієнту.

### Список параметрів

`request`

SOAP-запит. Якщо аргумент не заданий, передбачається, що запит знаходиться в необроблених POST-даних HTTP-запиту.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `request` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **SoapServer::handle()****

```php
<?php
function test($x)
{
    return $x;
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

### Дивіться також

-   [SoapServer::construct()](soapserver.construct.md) - Конструктор SoapServer