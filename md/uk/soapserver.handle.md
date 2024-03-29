---
navigation:
  - soapserver.getfunctions.md: '« SoapServer::getFunctions'
  - soapserver.setclass.md: 'SoapServer::setClass »'
  - index.md: PHP Manual
  - class.soapserver.md: SoapServer
title: 'SoapServer::handle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

SOAP-запит. Якщо аргумент не заданий, передбачається, що запит знаходиться у необроблених POST-даних HTTP-запиту.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `request` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** SoapServer::handle()\*\*\*\*

```php
<?php
function test($x)
{
    return $x;
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

### Дивіться також

-   [SoapServer::\_\_construct()](soapserver.construct.md) \- Конструктор SoapServer
