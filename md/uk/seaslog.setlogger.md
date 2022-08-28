Встановлює ім'я реєстратора SeasLog

-   [« SeasLog::setDatetimeFormat](seaslog.setdatetimeformat.html)
    
-   [SeasLog::setRequestID »](seaslog.setrequestid.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Встановлює ім'я реєстратора SeasLog
    

# SeasLog::setLogger

(PECL seaslog >=1.0.0)

SeasLog::setLogger — Встановлює ім'я реєстратора SeasLog

### Опис

```methodsynopsis
public static SeasLog::setLogger(string $logger): bool
```

Використання функції **SeasLog::setLogger()** змінить значення функції [SeasLog::getLastLogger()](seaslog.getlastlogger.html). Отже, SeasLog запише loginfo у каталог реєстратора.

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

-   [SeasLog::getLastLogger()](seaslog.getlastlogger.html) - Отримує останній шлях реєстратора SeasLog
-   [SeasLog::closeLoggerStream()](seaslog.closeloggerstream.html) - вручну звільняє потік від реєстратора