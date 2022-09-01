---
navigation:
  - seaslog.getdatetimeformat.md: '« SeasLog::getDatetimeFormat'
  - seaslog.getrequestid.md: 'SeasLog::getRequestID »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getLastLogger'
---
# SeasLog::getLastLogger

(PECL seaslog >=1.0.0)

SeasLog::getLastLogger — Отримує останній шлях реєстратора SeasLog

### Опис

```methodsynopsis
public static SeasLog::getLastLogger(): string
```

Використовуйте функцію **SeasLog::getLastLogger()**, щоб отримати значення [seaslog.defaultlogger](seaslog.configuration.html#ini.seaslog.default-logger), яке задано у php.ini (seaslog.ini).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Використання функції [SeasLog::setLogger()](seaslog.setlogger.md) змінить значення функції **SeasLog::getLastLogger()**

### Приклади

**Приклад #1 Приклад використання **SeasLog::getLastLogger()****

```php
<?php

var_dump(SeasLog::getLastLogger());
SeasLog::setLogger('theNewLogger');
var_dump(SeasLog::getLastLogger());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(7) "default"
string(12) "theNewLogger"
```

### Дивіться також

-   [SeasLog::setLogger()](seaslog.setlogger.md) - Встановлює ім'я реєстратора SeasLog
