---
navigation:
  - soapserver.handle.md: '« SoapServer::handle'
  - soapserver.setobject.md: 'SoapServer::setObject »'
  - index.md: PHP Manual
  - class.soapserver.md: SoapServer
title: 'SoapServer::setClass'
---
# SoapServer::setClass

(PHP 5, PHP 7, PHP 8)

SoapServer::setClass — Встановлює клас, який обробляє SOAP-запити

### Опис

```methodsynopsis
public SoapServer::setClass(string $class, mixed ...$args): void
```

Експортує всі методи із зазначеного класу.

Щоб зберегти об'єкт для кожного наступного запиту в рамках цієї PHP-сесії, можна використовувати метод [SoapServer::setPersistence()](soapserver.setpersistence.md)

### Список параметрів

`class`

Ім'я класу, що експортується.

`args`

Ці необов'язкові параметри будуть передані конструктору класу під час створення об'єкта.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [SoapServer::construct()](soapserver.construct.md) - Конструктор SoapServer
-   [SoapServer::addFunction()](soapserver.addfunction.md) - Додає одну або кілька функцій для обробки запитів SOAP
-   [SoapServer::setPersistence()](soapserver.setpersistence.md) - Встановлює режим збереження SoapServer
