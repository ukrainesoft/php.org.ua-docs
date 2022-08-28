Отримує останній шлях реєстратора SeasLog

-   [« SeasLog::getDatetimeFormat](seaslog.getdatetimeformat.html)
    
-   [SeasLog::getRequestID »](seaslog.getrequestid.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Отримує останній шлях реєстратора SeasLog
    

# SeasLog::getLastLogger

(PECL seaslog >=1.0.0)

SeasLog::getLastLogger — Отримує останній шлях реєстратора SeasLog

### Опис

```methodsynopsis
public static SeasLog::getLastLogger(): string
```

Використовуйте функцію **SeasLog::getLastLogger()**, щоб отримати значення [seaslog.default\_logger](seaslog.configuration.html#ini.seaslog.default-logger), яке задано у php.ini (seaslog.ini).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Використання функції [SeasLog::setLogger()](seaslog.setlogger.html) змінить значення функції **SeasLog::getLastLogger()**

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

-   [SeasLog::setLogger()](seaslog.setlogger.html) - Встановлює ім'я реєстратора SeasLog