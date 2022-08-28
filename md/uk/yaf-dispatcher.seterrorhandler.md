Встановлює обробник помилок

-   [« Yaf\_Dispatcher::setDefaultModule](yaf-dispatcher.setdefaultmodule.html)
    
-   [Yaf\_Dispatcher::setRequest »](yaf-dispatcher.setrequest.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Dispatcher](class.yaf-dispatcher.html)
    
-   Встановлює обробник помилок
    

# YafDispatcher::setErrorHandler

(Yaf >=1.0.0)

YafDispatcher::setErrorHandler — Встановлює обробник помилок

### Опис

```methodsynopsis
public Yaf_Dispatcher::setErrorHandler(call $callback, int $error_types): Yaf_Dispatcher
```

Встановлює обробник помилок Yaf. Якщо [application.dispatcher.throwException](yaf.appconfig.html#configuration.yaf.dispatcher.throwexception) вимкнений, Yaf буде викликати помилку, що перехоплюється, у разі виникнення непередбачених помилок.

Таким чином, цей обробник помилок буде викликатись у разі виникнення помилки.

### Список параметрів

`callback`

Callback-функція, що викликається

`error_types`

### Значення, що повертаються

### Дивіться також

-   [Yaf\_Dispatcher::throwException()](yaf-dispatcher.throwexception.html) - Вмикає/вимикає викидання винятків
-   [Yaf\_Application::getLastErrorNo()](yaf-application.getlasterrorno.html) - Отримати код останньої помилки
-   [Yaf\_Application::getLastErrorMsg()](yaf-application.getlasterrormsg.html) - Отримати останнє повідомлення про помилку