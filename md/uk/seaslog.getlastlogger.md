---
navigation:
  - seaslog.getdatetimeformat.md: '« SeasLog::getDatetimeFormat'
  - seaslog.getrequestid.md: 'SeasLog::getRequestID »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getLastLogger'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::getLastLogger

(PECL seaslog >=1.0.0)

SeasLog::getLastLogger — Отримує останній шлях реєстратора SeasLog

### Опис

```methodsynopsis
public static SeasLog::getLastLogger(): string
```

Используйте функцию**SeasLog::getLastLogger()**, щоб отримати значення [seaslog.default\_logger](seaslog.configuration.md#ini.seaslog.default-logger), яке задано у php.ini (seaslog.ini).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Использование функции[SeasLog::setLogger()](seaslog.setlogger.md)изменит значение функции**SeasLog::getLastLogger()**

### Приклади

**Приклад #1 Приклад використання** SeasLog::getLastLogger()\*\*\*\*

```php
<?php

var_dump(SeasLog::getLastLogger());
SeasLog::setLogger('theNewLogger');
var_dump(SeasLog::getLastLogger());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(7) "default"
string(12) "theNewLogger"
```

### Дивіться також

-   [SeasLog::setLogger()](seaslog.setlogger.md) \- Встановлює ім'я реєстратора SeasLog
