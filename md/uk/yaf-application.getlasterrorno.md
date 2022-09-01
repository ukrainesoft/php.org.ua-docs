---
navigation:
  - yaf-application.getlasterrormsg.html: '« YafApplication::getLastErrorMsg'
  - yaf-application.getmodules.html: 'YafApplication::getModules »'
  - index.html: PHP Manual
  - class.yaf-application.html: YafApplication
title: 'YafApplication::getLastErrorNo'
---
# YafApplication::getLastErrorNo

(Yaf> = 2.1.2)

YafApplication::getLastErrorNo — Отримати код останньої помилки

### Опис

```methodsynopsis
public Yaf_Application::getLastErrorNo(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafApplication::getLastErrorNo()****

```php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   var_dump(Yaf_Application::app()->getLastErrorNo());
   var_dump(Yaf_Application::app()->getLastErrorNo() == YAF_ERR_NOTFOUND_CONTROLLER);
}

$config = array(
  "application" => array(
   "directory" => "/tmp/notexists",
     "dispatcher" => array(
       "throwException" => 0, //вызывать ошибку вместо исключения
      ),
  ),
);

$app = new Yaf_Application($config);
$app->getDispatcher()->setErrorHandler("error_handler", E_RECOVERABLE_ERROR);
$app->run();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(516)
bool(true)
```
