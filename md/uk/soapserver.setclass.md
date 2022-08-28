Встановлює клас, який обробляє SOAP-запити

-   [« SoapServer::handle](soapserver.handle.html)
    
-   [SoapServer::setObject »](soapserver.setobject.html)
    
-   [PHP Manual](index.html)
    
-   [SoapServer](class.soapserver.html)
    
-   Встановлює клас, який обробляє SOAP-запити
    

# SoapServer::setClass

(PHP 5, PHP 7, PHP 8)

SoapServer::setClass — Встановлює клас, який обробляє SOAP-запити

### Опис

```methodsynopsis
public SoapServer::setClass(string $class, mixed ...$args): void
```

Експортує всі методи із зазначеного класу.

Щоб зберегти об'єкт для кожного наступного запиту в рамках цієї PHP-сесії, можна використовувати метод [SoapServer::setPersistence()](soapserver.setpersistence.html)

### Список параметрів

`class`

Ім'я класу, що експортується.

`args`

Ці необов'язкові параметри будуть передані конструктору класу під час створення об'єкта.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [SoapServer::\_\_construct()](soapserver.construct.html) - Конструктор SoapServer
-   [SoapServer::addFunction()](soapserver.addfunction.html) - Додає одну або кілька функцій для обробки запитів SOAP
-   [SoapServer::setPersistence()](soapserver.setpersistence.html) - Встановлює режим збереження SoapServer