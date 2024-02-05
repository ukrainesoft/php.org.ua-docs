---
navigation:
  - yaf-dispatcher.autorender.md: '« Yaf\_Dispatcher::autoRender'
  - yaf-dispatcher.construct.md: 'Yaf\_Dispatcher::\_\_construct »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.md: Yaf\_Dispatcher
title: 'Yaf\_Dispatcher::catchException'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Dispatcher::catchException

(Yaf >=1.0.0)

Yaf\_Dispatcher::catchException — Вмикає/вимикає перехоплення винятків

### Опис

```methodsynopsis
public Yaf_Dispatcher::catchException(bool $flag = ?): Yaf_Dispatcher
```

Поки включено application.dispatcher.throwException (ви також можете викликати **Yaf\_Dispatcher::throwException(TRUE)()**, щоб увімкнути), Yaf буде викидати виняток у разі виникнення помилки замість помилки спрацьовування.

тоді, якщо ви увімкнете **Yaf\_Dispatcher::catchException()**(также можно включить, установив[application.dispatcher.catchException](yaf.appconfig.md#configuration.yaf.dispatcher.catchexception)), всі неперехоплені винятки будуть спіймані ErrorController::error, якщо ви його визначили.

### Список параметрів

`flag`

Логічне значення

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Dispatcher::catchException()\*\*\*\*

```php
/* если вы определили ErrorController следующим образом */
<?php
class ErrorController extends Yaf_Controller_Abstract {
     /**
      * вы также можете вызвать Yaf_Request_Abstract::getException, чтобы получить
      * неперехваченное исключение.
      */
     public function errorAction($exception) {
        /* error occurs */
        switch ($exception->getCode()) {
            case YAF_ERR_NOTFOUND_MODULE:
            case YAF_ERR_NOTFOUND_CONTROLLER:
            case YAF_ERR_NOTFOUND_ACTION:
            case YAF_ERR_NOTFOUND_VIEW:
                echo 404, ":", $exception->getMessage();
                break;
            default :
                $message = $exception->getMessage();
                echo 0, ":", $exception->getMessage();
                break;
        }
     }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
/* now if some error occur, assuming access a non-exists controller(or you can throw a exception yourself): */
404:Could not find controller script **/application/controllers/No-exists-controller.php
```

### Дивіться також

-   [Yaf\_Dispatcher::throwException()](yaf-dispatcher.throwexception.md) \- Вмикає/вимикає викидання винятків
-   [Yaf\_Dispatcher::setErrorHandler()](yaf-dispatcher.seterrorhandler.md) \- Встановлює обробник помилок
