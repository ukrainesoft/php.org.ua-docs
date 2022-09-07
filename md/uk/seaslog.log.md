---
navigation:
  - seaslog.info.md: '« SeasLog::info'
  - seaslog.notice.md: 'SeasLog::notice »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::log'
---
# SeasLog::log

(PECL seaslog >=1.0.0)

SeasLog::log — Загальна функція запису до журналу

### Опис

```methodsynopsis
public static SeasLog::log(    string $level,    string $message = ?,    array $content = ?,    string $logger = ?): bool
```

Загальна функція запису журналу.

### Список параметрів

`level`

Можна використовувати рівень один із:

-   [SEASLOGDEBUG](seaslog.constants.md#constant.seaslog-debug)
-   [SEASLOGINFO](seaslog.constants.md#constant.seaslog-info)
-   [SEASLOGNOTICE](seaslog.constants.md#constant.seaslog-notice)
-   [SEASLOGWARNING](seaslog.constants.md#constant.seaslog-warning)
-   [SEASLOGERROR](seaslog.constants.md#constant.seaslog-error)
-   [SEASLOGCRITICAL](seaslog.constants.md#constant.seaslog-critical)
-   [SEASLOGALERT](seaslog.constants.md#constant.seaslog-alert)
-   [SEASLOGEMERGENCY](seaslog.constants.md#constant.seaslog-emergency)

Або ви можете створити власний рівень.

`message`

Повідомлення журналу.

`content`

Повідомлення містить заповнювачі, які заміняють розробники значеннями з масиву вмісту. Якщо message - це інформація журналу від {NAME}, а content array('NAME' => 'Микити'), інформація журналу буде інформація журналу від Микити

`logger`

logger, укладений у третій параметр, буде використовуватися зараз, як тимчасовий реєстратор, якщо функція SeasLog::setLogger() викликається у попередньому вмісті. Якщо logger дорівнює NULL або "" (порожній рядок), SeasLog використовуватиме останній реєстратор, встановлений методом [SeasLog::setLogger()](seaslog.setlogger.md)

### Значення, що повертаються

Повертає TRUE у разі успішного виконання запису журналу, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::log()****

```php
<?php

var_dump(SeasLog::log(SEASLOG_INFO,'info log'));
var_dump(SeasLog::getBuffer());

//создание нового собственного уровня
var_dump(SeasLog::log('MySelfLevel','info log'));
var_dump(SeasLog::getBuffer());

//с `content`
var_dump(SeasLog::log('MySelfLevel','info log {NAME}',array('NAME' => 'neeke')));
var_dump(SeasLog::getBuffer());

//с `logger`
var_dump(SeasLog::log('MySelfLevel','info log {NAME}',array('NAME' => 'neeke'),'tmp_logger'));
var_dump(SeasLog::getBuffer());


?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
array(1) {
  ["/var/log/www/default/20180707.log"]=>
  array(1) {
    [0]=>
    string(79) "2018-07-07 11:12:37 | INFO | 72427 | 5b402fa56a2ea | 1530933157.436 | info log
"
  }
}

bool(true)
array(1) {
  ["/var/log/www/default/20180707.log"]=>
  array(1) {
    [0]=>
    string(86) "2018-07-07 11:13:59 | MySelfLevel | 72470 | 5b402ff781c5e | 1530933239.532 | info log
"
  }
}

bool(true)
array(1) {
  ["/var/log/www/tmp_logger/20180707.log"]=>
  array(1) {
    [0]=>
    string(92) "2018-07-07 11:28:12 | MySelfLevel | 72833 | 5b40334ce6a2f | 1530934092.946 | info log neeke
"
  }
}

bool(true)
array(1) {
  ["/var/log/www/default/20180707.log"]=>
  array(1) {
    [0]=>
    string(86) "2018-07-07 11:20:12 | INFO | 72616 | 5b40316c3641e | 1530933612.222 | info log neeke
"
  }
}
```

### Дивіться також

-   [seaslog.defaulttemplate](seaslog.configuration.md#ini.seaslog.default-template)
-   [SeasLog::debug()](seaslog.debug.md) - Записує інформацію рівня "debug" до журналу
-   [SeasLog::info()](seaslog.info.md) - Записує інформацію рівня "info" до журналу
-   [SeasLog::notice()](seaslog.notice.md) - Записує інформацію рівня "notice" у журнал
-   [SeasLog::warning()](seaslog.warning.md) - Записує інформацію рівня "warning" до журналу
-   [SeasLog::error()](seaslog.error.md) - Записує інформацію рівня "error" у журнал
-   [SeasLog::critical()](seaslog.critical.md) - Записує інформацію рівня "critical" у журнал
-   [SeasLog::alert()](seaslog.alert.md) - Записує інформацію рівня "alert" у журнал
-   [SeasLog::emergency()](seaslog.emergency.md) - Записує інформацію рівня "emergency" до журналу
