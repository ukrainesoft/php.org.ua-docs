---
navigation:
  - yaf-application.getlasterrormsg.md: '« Yaf\_Application::getLastErrorMsg'
  - yaf-application.getmodules.md: 'Yaf\_Application::getModules »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::getLastErrorNo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::getLastErrorNo

(Yaf >=2.1.2)

Yaf\_Application::getLastErrorNo — Отримати код останньої помилки

### Опис

```methodsynopsis
public Yaf_Application::getLastErrorNo(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Application::getLastErrorNo()\*\*\*\*

```php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   var_dump(Yaf_Application::app()->getLastErrorNo());
   var_dump(Yaf_Application::app()->getLastErrorNo() == YAF_ERR_NOTFOUND_CONTROLLER);
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
int(516)
bool(true)
```
