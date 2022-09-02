---
navigation:
  - class.seaslog.md: « SeasLog
  - seaslog.analyzercount.md: 'SeasLog::analyzerCount »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::alert'
---
# SeasLog::alert

(PECL seaslog >=1.0.0)

SeasLog::alert — записує інформацію рівня "alert" до журналу

### Опис

```methodsynopsis
public static SeasLog::alert(string $message, array $content = ?, string $logger = ?): bool
```

Записує інформацію рівня "alert" у журнал.

> **Зауваження**
> 
> "ALERT" - Дії мають бути здійснені негайно. Негайну увагу слід приділяти персоналу для аварійного ремонту.

### Список параметрів

`message`

Повідомлення журналу.

`content`

Повідомлення містить заповнювачі, які заміняють розробники значеннями з масиву вмісту. Якщо message - це інформація журналу від {NAME}, а content array('NAME' => 'Микити'), інформація журналу буде інформація журналу від Микити

`logger`

logger, укладений у третій параметр, буде використовуватися зараз, як тимчасовий реєстратор, якщо функція SeasLog::setLogger() викликається у попередньому вмісті. Якщо logger дорівнює NULL або "" (порожній рядок), SeasLog використовуватиме останній реєстратор, встановлений методом [SeasLog::setLogger()](seaslog.setlogger.md)

### Значення, що повертаються

Повертає TRUE у разі успішного виконання запису журналу, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::alert()****

```php
<?php

var_dump(SeasLog::alert('log message'));

//с content
var_dump(SeasLog::alert('log message from {NAME}',array('NAME' => 'neeke')));

//с временным logger
var_dump(SeasLog::alert('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
bool(true)
array(2) {
  ["/var/log/www/default/20180707.log"]=>
  array(2) {
    [0]=>
    string(81) "2018-07-07 11:45:49 | ALERT | 73263 | 5b40376d1067c | 1530935149.68 | log message
"
    [1]=>
    string(92) "2018-07-07 11:45:49 | ALERT | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
"
  }
  ["/var/log/www/tmp_logger/20180707.log"]=>
  array(1) {
    [0]=>
    string(92) "2018-07-07 11:45:49 | ALERT | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
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
-   [SeasLog::emergency()](seaslog.emergency.md) - Записує інформацію рівня "emergency" до журналу
-   [SeasLog::log()](seaslog.log.md) - Загальна функція запису до журналу
