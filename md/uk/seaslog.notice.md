---
navigation:
  - seaslog.log.md: '« SeasLog::log'
  - seaslog.setbasepath.md: 'SeasLog::setBasePath »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::notice'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::notice

(PECL seaslog >=1.0.0)

SeasLog::notice — Записує інформацію рівня "notice" у журнал

### Опис

```methodsynopsis
public static SeasLog::notice(string $message, array $content = ?, string $logger = ?): bool
```

Записує інформацію рівня "notice" у журнал.

> **Зауваження** :
> 
> "NOTICE" - нормальні, але важливі події. Інформація, яка важливіша за рівень "info" під час виконання.

### Список параметрів

`message`

Повідомлення журналу.

`content`

Повідомлення містить заповнювачі, які розробники замінюють значеннями масиву вмісту. Якщо \`message\` - це \`інформація журналу від {NAME}\`, а\`content\` \`array('NAME' => 'Микити')\`, інформація журналу буде \`інформація журналу від Микити\`

`logger`

\`logger\`, укладений у третій параметр, буде використовуватися зараз, як тимчасовий реєстратор, якщо функція SeasLog::setLogger() викликається у попередньому вмісті. Якщо \`logger\` дорівнює NULL або "" (порожній рядок), SeasLog використовуватиме останній реєстратор, встановлений методом [SeasLog::setLogger()](seaslog.setlogger.md)

### Значення, що повертаються

Повертає TRUE у разі успішного виконання запису журналу, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** SeasLog::notice()\*\*\*\*

```php
<?php

var_dump(SeasLog::notice('log message'));

//с content
var_dump(SeasLog::notice('log message from {NAME}',array('NAME' => 'neeke')));

//с временным logger
var_dump(SeasLog::notice('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
bool(true)
array(2) {
  ["/var/log/www/default/20180707.log"]=>
  array(2) {
    [0]=>
    string(81) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message
"
    [1]=>
    string(92) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
"
  }
  ["/var/log/www/tmp_logger/20180707.log"]=>
  array(1) {
    [0]=>
    string(92) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
"
  }
}
```

### Дивіться також

-   [seaslog.default\_template](seaslog.configuration.md#ini.seaslog.default-template)
-   [SeasLog::debug()](seaslog.debug.md) - Записує інформацію рівня "debug" до журналу
-   [SeasLog::info()](seaslog.info.md) - Записує інформацію рівня "info" до журналу
-   [SeasLog::warning()](seaslog.warning.md) - Записує інформацію рівня "warning" до журналу
-   [SeasLog::error()](seaslog.error.md) - Записує інформацію рівня "error" у журнал
-   [SeasLog::critical()](seaslog.critical.md) - Записує інформацію рівня "critical" у журнал
-   [SeasLog::alert()](seaslog.alert.md) - Записує інформацію рівня "alert" у журнал
-   [SeasLog::emergency()](seaslog.emergency.md) - Записує інформацію рівня "emergency" до журналу
-   [SeasLog::log()](seaslog.log.md) \- Загальна функція запису до журналу
