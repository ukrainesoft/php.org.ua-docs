---
navigation:
  - yaf-dispatcher.setdefaultmodule.md: '« Yaf\_Dispatcher::setDefaultModule'
  - yaf-dispatcher.setrequest.md: 'Yaf\_Dispatcher::setRequest »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.md: Yaf\_Dispatcher
title: 'Yaf\_Dispatcher::setErrorHandler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Dispatcher::setErrorHandler

(Yaf >=1.0.0)

Yaf\_Dispatcher::setErrorHandler — Встановлює обробник помилок

### Опис

```methodsynopsis
public Yaf_Dispatcher::setErrorHandler(call $callback, int $error_types): Yaf_Dispatcher
```

Устанавливает обработчик ошибок для Yaf. Если[application.dispatcher.throwException](yaf.appconfig.md#configuration.yaf.dispatcher.throwexception) вимкнений, Yaf викликатиме перехоплювану помилку у разі виникнення непередбачених помилок.

Таким чином, цей обробник помилок буде викликатись у разі виникнення помилки.

### Список параметрів

`callback`

Callback-функція, що викликається

`error_types`

### Значення, що повертаються

### Дивіться також

-   [Yaf\_Dispatcher::throwException()](yaf-dispatcher.throwexception.md) \- Вмикає/вимикає викидання винятків
-   [Yaf\_Application::getLastErrorNo()](yaf-application.getlasterrorno.md) \- Отримати код останньої помилки
-   [Yaf\_Application::getLastErrorMsg()](yaf-application.getlasterrormsg.md) \- Отримати останнє повідомлення про помилку
