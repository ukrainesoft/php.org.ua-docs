Отримати останнє повідомлення про помилку

-   [« Yaf\_Application::getDispatcher](yaf-application.getdispatcher.html)
    
-   [Yaf\_Application::getLastErrorNo »](yaf-application.getlasterrorno.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Application](class.yaf-application.html)
    
-   Отримати останнє повідомлення про помилку
    

# YafApplication::getLastErrorMsg

(Yaf> = 2.1.2)

YafApplication::getLastErrorMsg — Отримати останнє повідомлення про помилку

### Опис

```methodsynopsis
public Yaf_Application::getLastErrorMsg(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafApplication::getLastErrorMsg()****

```php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   var_dump(Yaf_Application::app()->getLastErrorMsg());
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
string(69) "Could not find controller script /tmp/notexists/controllers/Index.php"
```