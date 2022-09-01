---
navigation:
  - yaf-dispatcher.setview.html: '« YafDispatcher::setView'
  - class.yaf-config-abstract.html: YafConfigAbstract »
  - index.md: PHP Manual
  - class.yaf-dispatcher.html: YafDispatcher
title: 'YafDispatcher::throwException'
---
# YafDispatcher::throwException

(Yaf >=1.0.0)

YafDispatcher::throwException — Вмикає/вимикає викидання винятків

### Опис

```methodsynopsis
public Yaf_Dispatcher::throwException(bool $flag = ?): Yaf_Dispatcher
```

Вмикає/вимикає викидання винятків у разі виникнення непередбаченої помилки. Коли увімкнено, Yaf буде викидати винятки замість того, щоб викликати помилки, які можна відловити.

Ви також можете використовувати [application.dispatcher.throwException](yaf.appconfig.html#configuration.yaf.dispatcher.throwexception), щоб досягти тієї ж мети.

### Список параметрів

`flag`

bool

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafDispatcher::throwexception()****

```php
<?php

$config = array(
    'application' => array(
        'directory' => dirname(__FILE__),
    ),
);
$app = new Yaf_Application($config);

$app->getDispatcher()->throwException(true);

try {
    $app->run();
} catch (Yaf_Exception $e) {
    var_dump($e->getMessage());
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(59) "Could not find controller script /tmp/controllers/Index.php"
```

**Приклад #2 Приклад використання **YafDispatcher::throwexception()****

```php
<?php

$config = array(
    'application' => array(
        'directory' => dirname(__FILE__),
    ),
);
$app = new Yaf_Application($config);

$app->getDispatcher()->throwException(false);

$app->run();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
PHP Catchable fatal error:  Yaf_Application::run(): Could not find controller script /tmp/controllers/Index.php in /tmp/1.php on line 12
```

### Дивіться також

-   [YafDispatcher::catchException()](yaf-dispatcher.catchexception.md) - Включає/вимикає перехоплення винятків
-   [YafException](class.yaf-exception.md)
