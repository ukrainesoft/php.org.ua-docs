---
navigation:
  - yaf-application.app.md: '« YafApplication::app'
  - yaf-application.clearlasterror.md: 'YafApplication::clearLastError »'
  - index.md: PHP Manual
  - class.yaf-application.md: YafApplication
title: 'YafApplication::bootstrap'
---
# YafApplication::bootstrap

(Yaf >=1.0.0)

YafApplication::bootstrap — Викликати bootstrap

### Опис

```methodsynopsis
public Yaf_Application::bootstrap(Yaf_Bootstrap_Abstract $bootstrap = ?): void
```

Запускає Bootstrap, всі методи, визначені в Bootstrap і іменовані з префіксом.init" будуть викликані в порядку їх визначення. Якщо параметр bootstrap не заданий, Yaf його шукатиме по шляху, вказаному в application.directory.

### Список параметрів

`bootstrap`

Екземпляр класу [YafBootstrapAbstract](class.yaf-bootstrap-abstract.md)

### Значення, що повертаються

Екземпляр класу [YafApplication](class.yaf-application.md)

### Приклади

**Приклад #1 Приклад використання **Bootstrap()****

```php
<?php
/**
 * Этот файл должен находиться по пути APPLICATION_PATH . "/application/"
 * (который определён в конфигурационном файле приложения Yaf_Application).
 * и называться Bootstrap.php, чтобы Yaf_Application смог его найти
 */
class Bootstrap extends Yaf_Bootstrap_Abstract {
    function _initConfig(Yaf_Dispatcher $dispatcher) {
        echo "первый метод вызван\n";
    }

    function _initPlugin($dispatcher) {
        echo "второй метод вызван\n";
    }
}
?>
```

**Приклад #2 Приклад використання **YafApplication::bootstrap()****

```php
<?php

defined('APPLICATION_PATH') // Будет использован APPLICATION_PATH
    || define('APPLICATION_PATH', __DIR__);

$application = new Yaf_Application(APPLICATION_PATH.'/conf/application.ini');
$application->bootstrap();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
первый метод вызван
второй метод вызван
```

### Дивіться також

-   [YafBootstrapAbstract](class.yaf-bootstrap-abstract.md)
