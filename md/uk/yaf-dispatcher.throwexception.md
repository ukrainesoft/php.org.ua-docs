---
navigation:
  - yaf-dispatcher.setview.md: '« Yaf\_Dispatcher::setView'
  - class.yaf-config-abstract.md: Yaf\_Config\_Abstract »
  - index.md: PHP Manual
  - class.yaf-dispatcher.md: Yaf\_Dispatcher
title: 'Yaf\_Dispatcher::throwException'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Dispatcher::throwException

(Yaf >=1.0.0)

Yaf\_Dispatcher::throwException — Вмикає/вимикає викидання винятків

### Опис

```methodsynopsis
public Yaf_Dispatcher::throwException(bool $flag = ?): Yaf_Dispatcher
```

Вмикає/вимикає викидання винятків у разі виникнення непередбаченої помилки. Коли увімкнено, Yaf буде викидати винятки замість того, щоб викликати помилки, які можна відловити.

Ви також можете використовувати [application.dispatcher.throwException](yaf.appconfig.md#configuration.yaf.dispatcher.throwexception), щоб досягти тієї ж мети.

### Список параметрів

`flag`

bool

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Yaf\_Dispatcher::throwexception()\*\*\*\*

```php
<?php

$config = array(
    'application' => array(
        'directory' => dirname(__FILE__),
    ),
);
$app = new Yaf_Application($config);

$app->getDispatcher()->throwException(true);

try {
    $app->run();
} catch (Yaf_Exception $e) {
    var_dump($e->getMessage());
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(59) "Could not find controller script /tmp/controllers/Index.php"
```

**Приклад #2 Приклад використання** Yaf\_Dispatcher::throwexception()\*\*\*\*

```php
<?php

$config = array(
    'application' => array(
        'directory' => dirname(__FILE__),
    ),
);
$app = new Yaf_Application($config);

$app->getDispatcher()->throwException(false);

$app->run();
?>
```

Висновок наведеного прикладу буде схожим на:

```
PHP Catchable fatal error:  Yaf_Application::run(): Could not find controller script /tmp/controllers/Index.php in /tmp/1.php on line 12
```

### Дивіться також

-   [Yaf\_Dispatcher::catchException()](yaf-dispatcher.catchexception.md) \- Включає/вимикає перехоплення винятків
-   [Yaf\_Exception](class.yaf-exception.md)
