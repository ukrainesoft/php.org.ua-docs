---
navigation:
  - yaf-dispatcher.autorender.html: '« YafDispatcher::autoRender'
  - yaf-dispatcher.construct.html: 'YafDispatcher::construct »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.html: YafDispatcher
title: 'YafDispatcher::catchException'
---
# YafDispatcher::catchException

(Yaf >=1.0.0)

YafDispatcher::catchException — Вмикає/вимикає перехоплення винятків

### Опис

```methodsynopsis
public Yaf_Dispatcher::catchException(bool $flag = ?): Yaf_Dispatcher
```

Поки включено application.dispatcher.throwException (ви також можете викликати **YafDispatcher::throwException(TRUE)()**, щоб увімкнути), Yaf буде викидати виняток у разі виникнення помилки замість помилки спрацьовування.

тоді, якщо ви увімкнете **YafDispatcher::catchException()** (також можна увімкнути, встановивши [application.dispatcher.catchException](yaf.appconfig.html#configuration.yaf.dispatcher.catchexception)), всі неперехоплені винятки будуть спіймані ErrorController::error, якщо ви його визначили.

### Список параметрів

`flag`

Логічне значення

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafDispatcher::catchException()****

```php
/* если вы определили ErrorController следующим образом */
<?php
class ErrorController extends Yaf_Controller_Abstract {
     /**
      * вы также можете вызвать Yaf_Request_Abstract::getException, чтобы получить
      * неперехваченное исключение.
      */
     public function errorAction($exception) {
        /* error occurs */
        switch ($exception->getCode()) {
            case YAF_ERR_NOTFOUND_MODULE:
            case YAF_ERR_NOTFOUND_CONTROLLER:
            case YAF_ERR_NOTFOUND_ACTION:
            case YAF_ERR_NOTFOUND_VIEW:
                echo 404, ":", $exception->getMessage();
                break;
            default :
                $message = $exception->getMessage();
                echo 0, ":", $exception->getMessage();
                break;
        }
     }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/* now if some error occur, assuming access a non-exists controller(or you can throw a exception yourself): */
404:Could not find controller script **/application/controllers/No-exists-controller.php
```

### Дивіться також

-   [YafDispatcher::throwException()](yaf-dispatcher.throwexception.html) - Вмикає/вимикає викидання винятків
-   [YafDispatcher::setErrorHandler()](yaf-dispatcher.seterrorhandler.html) - Встановлює обробник помилок
