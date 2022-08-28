Записує інформацію рівня "warning" до журналу

-   [« SeasLog::setRequestVariable](seaslog.setrequestvariable.html)
    
-   [SPL »](book.spl.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Записує інформацію рівня "warning" до журналу
    

# SeasLog::warning

(PECL seaslog >=1.0.0)

SeasLog::warning — записує інформацію рівня "warning" до журналу

### Опис

```methodsynopsis
public static SeasLog::warning(string $message, array $content = ?, string $logger = ?): bool
```

Записує інформацію рівня "warning" у журнал.

> **Зауваження**
> 
> "WARNING" - Виняткові випадки, які є помилками. Потенційно помилкова інформація, яка потребує уваги та потребує виправлення.

### Список параметрів

`message`

Повідомлення журналу.

`content`

Повідомлення містить заповнювачі, які заміняють розробники значеннями з масиву вмісту. Якщо message - це інформація журналу від {NAME}, а content array('NAME' => 'Микити'), інформація журналу буде інформація журналу від Микити

`logger`

logger, укладений у третій параметр, буде використовуватися зараз, як тимчасовий реєстратор, якщо функція SeasLog::setLogger() викликається у попередньому вмісті. Якщо logger дорівнює NULL або "" (порожній рядок), SeasLog використовуватиме останній реєстратор, встановлений методом [SeasLog::setLogger()](seaslog.setlogger.html)

### Значення, що повертаються

Повертає TRUE у разі успішного виконання запису журналу, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::warning()****

```php
<?php

var_dump(SeasLog::warning('log message'));

//с content
var_dump(SeasLog::warning('log message from {NAME}',array('NAME' => 'neeke')));

//с временным logger
var_dump(SeasLog::warning('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

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
    string(81) "2018-07-07 11:45:49 | WARNING | 73263 | 5b40376d1067c | 1530935149.68 | log message
"
    [1]=>
    string(92) "2018-07-07 11:45:49 | WARNING | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
"
  }
  ["/var/log/www/tmp_logger/20180707.log"]=>
  array(1) {
    [0]=>
    string(92) "2018-07-07 11:45:49 | WARNING | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
"
  }
}
```

### Дивіться також

-   [seaslog.default\_template](seaslog.configuration.html#ini.seaslog.default-template)
-   [SeasLog::debug()](seaslog.debug.html) - Записує інформацію рівня "debug" до журналу
-   [SeasLog::info()](seaslog.info.html) - Записує інформацію рівня "info" до журналу
-   [SeasLog::notice()](seaslog.notice.html) - Записує інформацію рівня "notice" у журнал
-   [SeasLog::error()](seaslog.error.html) - Записує інформацію рівня "error" у журнал
-   [SeasLog::critical()](seaslog.critical.html) - Записує інформацію рівня "critical" у журнал
-   [SeasLog::alert()](seaslog.alert.html) - Записує інформацію рівня "alert" у журнал
-   [SeasLog::emergency()](seaslog.emergency.html) - Записує інформацію рівня "emergency" до журналу
-   [SeasLog::log()](seaslog.log.html) - Загальна функція запису до журналу