---
navigation:
  - soapserver.fault.md: '« SoapServer::fault'
  - soapserver.handle.md: 'SoapServer::handle »'
  - index.md: PHP Manual
  - class.soapserver.md: SoapServer
title: 'SoapServer::getFunctions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapServer::getFunctions

(PHP 5, PHP 7, PHP 8)

SoapServer::getFunctions — Повернути список функцій

### Опис

```methodsynopsis
public SoapServer::getFunctions(): array
```

Повернути список функцій в об'єкті SoapServer. Цей метод повертає список усіх функцій, доданих за допомогою [SoapServer::addFunction()](soapserver.addfunction.md) або [SoapServer::setClass()](soapserver.setclass.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

`Масив` певних функцій.

### Приклади

**Пример #1 Пример использования**SoapServer::getFunctions()\*\*\*\*

```php
<?php
$server = new SoapServer(NULL, array("uri" => "http://test-uri"));
$server->addFunction(SOAP_FUNCTIONS_ALL);
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  $server->handle();
} else {
  echo "Этот сервер SOAP может обрабатывать следующие функции: ";
  $functions = $server->getFunctions();
  foreach($functions as $func) {
    echo $func . "\n";
  }
}
?>
```

### Дивіться також

-   [SoapServer::\_\_construct()](soapserver.construct.md) \- Конструктор SoapServer
-   [SoapServer::addFunction()](soapserver.addfunction.md) \- Додає одну або кілька функцій для обробки запитів SOAP
-   [SoapServer::setClass()](soapserver.setclass.md) \- Встановлює клас, який обробляє SOAP-запити
