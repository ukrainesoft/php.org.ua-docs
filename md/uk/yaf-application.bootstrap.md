---
navigation:
  - yaf-application.app.md: '« Yaf\_Application::app'
  - yaf-application.clearlasterror.md: 'Yaf\_Application::clearLastError »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::bootstrap'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::bootstrap

(Yaf >=1.0.0)

Yaf\_Application::bootstrap — Викликати bootstrap

### Опис

```methodsynopsis
public Yaf_Application::bootstrap(Yaf_Bootstrap_Abstract $bootstrap = ?): void
```

Запускає Bootstrap, всі методи, визначені в Bootstrap і іменовані з префіксом.\_init" будуть викликані в порядку їх визначення. Якщо параметр bootstrap не заданий, Yaf його шукатиме по шляху, вказаному в application.directory.

### Список параметрів

`bootstrap`

Екземпляр класу [Yaf\_Bootstrap\_Abstract](class.yaf-bootstrap-abstract.md)

### Значення, що повертаються

Екземпляр класу [Yaf\_Application](class.yaf-application.md)

### Приклади

**Приклад #1 Приклад використання** Bootstrap()\*\*\*\*

```php
<?php
/**
 * Этот файл должен находиться по пути APPLICATION_PATH . "/application/"
 * (который определён в конфигурационном файле приложения Yaf_Application).
 * и называться Bootstrap.php, чтобы Yaf_Application смог его найти
 */
class Bootstrap extends Yaf_Bootstrap_Abstract {
    function _initConfig(Yaf_Dispatcher $dispatcher) {
        echo "первый метод вызван\n";
    }

    function _initPlugin($dispatcher) {
        echo "второй метод вызван\n";
    }
}
?>
```

**Приклад #2 Приклад використання** Yaf\_Application::bootstrap()\*\*\*\*

```php
<?php

defined('APPLICATION_PATH') // Будет использован APPLICATION_PATH
    || define('APPLICATION_PATH', __DIR__);

$application = new Yaf_Application(APPLICATION_PATH.'/conf/application.ini');
$application->bootstrap();
?>
```

Висновок наведеного прикладу буде схожим на:

```
первый метод вызван
второй метод вызван
```

### Дивіться також

-   [Yaf\_Bootstrap\_Abstract](class.yaf-bootstrap-abstract.md)
