---
navigation:
  - seaslog.setdatetimeformat.md: '« SeasLog::setDatetimeFormat'
  - seaslog.setrequestid.md: 'SeasLog::setRequestID »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::setLogger'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::setLogger

(PECL seaslog >=1.0.0)

SeasLog::setLogger — Встановлює ім'я реєстратора SeasLog

### Опис

```methodsynopsis
public static SeasLog::setLogger(string $logger): bool
```

Использование функции\*\*SeasLog::setLogger()\*\*изменит значение функции[SeasLog::getLastLogger()](seaslog.getlastlogger.md). Отже, SeasLog запише loginfo у каталог реєстратора.

### Список параметрів

`logger`

Ім'я реєстратора.

### Значення, що повертаються

Повертає TRUE у разі успішного створення директорії реєстратора, FALSE у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**SeasLog::setLogger()\*\*\*\*

```php
<?php

var_dump(SeasLog::setLogger('testModule/testLogger'));

?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
```

### Дивіться також

-   [SeasLog::getLastLogger()](seaslog.getlastlogger.md) \- Отримує останній шлях реєстратора SeasLog
-   [SeasLog::closeLoggerStream()](seaslog.closeloggerstream.md) \- вручну звільняє потік від реєстратора
