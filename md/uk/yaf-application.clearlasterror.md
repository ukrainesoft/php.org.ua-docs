---
navigation:
  - yaf-application.bootstrap.md: '« Yaf\_Application::bootstrap'
  - yaf-application.construct.md: 'Yaf\_Application::\_\_construct »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::clearLastError'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::clearLastError

(Yaf >=2.1.2)

Yaf\_Application::clearLastError — Очищення інформації з останньої помилки

### Опис

```methodsynopsis
public Yaf_Application::clearLastError(): Yaf_Application
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Application::clearLastError()\*\*\*\*

```php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   Yaf_Application::app()->clearLastError();
   var_dump(Yaf_Application::app()->getLastErrorNo());
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
int(0)
```
