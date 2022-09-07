---
navigation:
  - yaf-dispatcher.setdefaultmodule.md: '« YafDispatcher::setDefaultModule'
  - yaf-dispatcher.setrequest.md: 'YafDispatcher::setRequest »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.md: YafDispatcher
title: 'YafDispatcher::setErrorHandler'
---
# YafDispatcher::setErrorHandler

(Yaf >=1.0.0)

YafDispatcher::setErrorHandler — Встановлює обробник помилок

### Опис

```methodsynopsis
public Yaf_Dispatcher::setErrorHandler(call $callback, int $error_types): Yaf_Dispatcher
```

Встановлює обробник помилок Yaf. Якщо [application.dispatcher.throwException](yaf.appconfig.md#configuration.yaf.dispatcher.throwexception) вимкнений, Yaf буде викликати помилку, що перехоплюється, у разі виникнення непередбачених помилок.

Таким чином, цей обробник помилок буде викликатись у разі виникнення помилки.

### Список параметрів

`callback`

Callback-функція, що викликається

`error_types`

### Значення, що повертаються

### Дивіться також

-   [YafDispatcher::throwException()](yaf-dispatcher.throwexception.md) - Вмикає/вимикає викидання винятків
-   [YafApplication::getLastErrorNo()](yaf-application.getlasterrorno.md) - Отримати код останньої помилки
-   [YafApplication::getLastErrorMsg()](yaf-application.getlasterrormsg.md) - Отримати останнє повідомлення про помилку
