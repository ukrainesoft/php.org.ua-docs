---
navigation:
  - seaslog.setdatetimeformat.md: '« SeasLog::setDatetimeFormat'
  - seaslog.setrequestid.md: 'SeasLog::setRequestID »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::setLogger'
---
# SeasLog::setLogger

(PECL seaslog >=1.0.0)

SeasLog::setLogger — Встановлює ім'я реєстратора SeasLog

### Опис

```methodsynopsis
public static SeasLog::setLogger(string $logger): bool
```

Використання функції **SeasLog::setLogger()** змінить значення функції [SeasLog::getLastLogger()](seaslog.getlastlogger.md). Отже, SeasLog запише loginfo у каталог реєстратора.

### Список параметрів

`logger`

Ім'я реєстратора.

### Значення, що повертаються

Повертає TRUE у разі успішного створення директорії реєстратора, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::setLogger()****

```php
<?php

var_dump(SeasLog::setLogger('testModule/testLogger'));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
```

### Дивіться також

-   [SeasLog::getLastLogger()](seaslog.getlastlogger.md) - Отримує останній шлях реєстратора SeasLog
-   [SeasLog::closeLoggerStream()](seaslog.closeloggerstream.md) - вручну звільняє потік від реєстратора
