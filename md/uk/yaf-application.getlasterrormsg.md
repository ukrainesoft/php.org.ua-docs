---
navigation:
  - yaf-application.getdispatcher.md: '« Yaf\_Application::getDispatcher'
  - yaf-application.getlasterrorno.md: 'Yaf\_Application::getLastErrorNo »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::getLastErrorMsg'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::getLastErrorMsg

(Yaf >=2.1.2)

Yaf\_Application::getLastErrorMsg — Отримати останнє повідомлення про помилку

### Опис

```methodsynopsis
public Yaf_Application::getLastErrorMsg(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Yaf\_Application::getLastErrorMsg()\*\*\*\*

```php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   var_dump(Yaf_Application::app()->getLastErrorMsg());
}

$config = array(
 "application" => array(
   "directory" => "/tmp/notexists",
     "dispatcher" => array(
       "throwException" => 0, //вызывать ошибку вместо исключения
      ),
  ),
);

$app = new Yaf_Application($config);
$app->getDispatcher()->setErrorHandler("error_handler", E_RECOVERABLE_ERROR);
$app->run();
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(69) "Could not find controller script /tmp/notexists/controllers/Index.php"
```
