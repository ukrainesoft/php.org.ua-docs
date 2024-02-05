---
navigation:
  - seaslog.analyzerdetail.md: '« SeasLog::analyzerDetail'
  - seaslog.construct.md: 'SeasLog::\_\_construct »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::closeLoggerStream'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::closeLoggerStream

(PECL seaslog >=1.8.6)

SeasLog::closeLoggerStream - Вручну звільняє потік від реєстратора

### Опис

```methodsynopsis
public static SeasLog::closeLoggerStream(int $model, string $logger): bool
```

Вручну звільняє потік від реєстратора. SeasLog кешує дескриптор потоку, відкритий реєстратором журналу, щоб заощадити витрати на створення потоку. Дескриптор буде автоматично звільнено наприкінці запиту. У режимі CLI процес автоматично завершиться при виході. Або ви можете використовувати такі функції для звільнення вручну (функція ручного звільнення потребує оновлення SeasLog до версії 1.8.6 або оновленої версії).

### Список параметрів

`model`

Ціла кількість, одна з констант:

-   [SEASLOG\_CLOSE\_LOGGER\_STREAM\_MOD\_ALL](seaslog.constants.md#constant.seaslog-close-logger-stream-mod-all)
-   [SEASLOG\_CLOSE\_LOGGER\_STREAM\_MOD\_ASSIGN](seaslog.constants.md#constant.seaslog-close-logger-stream-mod-assign)

`logger`

Ім'я реєстратора.

### Значення, що повертаються

Повертає TRUE у разі успішного звільнення потоку, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** SeasLog::closeLoggerStream()\*\*\*\*

```php
<?php

var_dump(SeasLog::closeLoggerStream());
var_dump(SeasLog::closeLoggerStream(SEASLOG_CLOSE_LOGGER_STREAM_MOD_ALL));
var_dump(SeasLog::closeLoggerStream(SEASLOG_CLOSE_LOGGER_STREAM_MOD_ASSIGN, 'logger_name'));

?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
bool(true)
```

### Дивіться також

-   [SeasLog::setLogger()](seaslog.setlogger.md) \- Встановлює ім'я реєстратора SeasLog
-   [SeasLog::getLastLogger()](seaslog.getlastlogger.md) \- Отримує останній шлях реєстратора SeasLog
