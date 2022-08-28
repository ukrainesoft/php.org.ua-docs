Очищення інформації з останньої помилки

-   [« Yaf\_Application::bootstrap](yaf-application.bootstrap.html)
    
-   [Yaf\_Application::\_\_construct »](yaf-application.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Application](class.yaf-application.html)
    
-   Очищення інформації з останньої помилки
    

# YafApplication::clearLastError

(Yaf> = 2.1.2)

YafApplication::clearLastError — Очищення інформації з останньої помилки

### Опис

```methodsynopsis
public Yaf_Application::clearLastError(): Yaf_Application
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafApplication::clearLastError()****

```php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   Yaf_Application::app()->clearLastError();
   var_dump(Yaf_Application::app()->getLastErrorNo());
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
int(0)
```