Повернути список певних функцій

-   [« SoapServer::fault](soapserver.fault.html)
    
-   [SoapServer::handle »](soapserver.handle.html)
    
-   [PHP Manual](index.html)
    
-   [SoapServer](class.soapserver.html)
    
-   Повернути список певних функцій
    

# SoapServer::getFunctions

(PHP 5, PHP 7, PHP 8)

SoapServer::getFunctions — Повернути список функцій

### Опис

```methodsynopsis
public SoapServer::getFunctions(): array
```

Повернути список функцій в об'єкті SoapServer. Цей метод повертає список усіх функцій, доданих за допомогою [SoapServer::addFunction()](soapserver.addfunction.html) або [SoapServer::setClass()](soapserver.setclass.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

`Массив` певних функцій.

### Приклади

**Приклад #1 Приклад використання **SoapServer::getFunctions()****

```php
<?php
$server = new SoapServer(NULL, array("uri" => "http://test-uri"));
$server->addFunction(SOAP_FUNCTIONS_ALL);
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  $server->handle();
} else {
  echo "Этот сервер SOAP может обрабатывать следующие функции: ";
  $functions = $server->getFunctions();
  foreach($functions as $func) {
    echo $func . "\n";
  }
}
?>
```

### Дивіться також

-   [SoapServer::\_\_construct()](soapserver.construct.html) - Конструктор SoapServer
-   [SoapServer::addFunction()](soapserver.addfunction.html) - Додає одну або кілька функцій для обробки запитів SOAP
-   [SoapServer::setClass()](soapserver.setclass.html) - Встановлює клас, який обробляє SOAP-запити