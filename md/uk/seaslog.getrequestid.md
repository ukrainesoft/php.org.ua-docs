Отримує диференційовані запити SeasLog requestід

-   [« SeasLog::getLastLogger](seaslog.getlastlogger.html)
    
-   [SeasLog::getRequestVariable »](seaslog.getrequestvariable.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Отримує диференційовані запити SeasLog requestід
    

# SeasLog::getRequestID

(PECL seaslog >=1.0.0)

SeasLog::getRequestID — Отримує диференційовані запити SeasLog requestід

### Опис

```methodsynopsis
public static SeasLog::getRequestID(): string
```

Щоб відрізнити один запит, наприклад, не викликати функції [SeasLog::setRequestId()](seaslog.setrequestid.html), при ініціалізації запиту використовується унікальне значення, що генерується вбудованою функцією static char getuniqid()

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, створений вбудованою функцією static char getuniqid() або задану функцією [SeasLog::setRequestId()](seaslog.setrequestid.html)

### Приклади

**Приклад #1 Приклад використання **SeasLog::getRequestID()****

```php
<?php

var_dump(SeasLog::getRequestID());
var_dump(SeasLog::setRequestID('reqeust_id_test_'.time()));
var_dump(SeasLog::getRequestID());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(13) "5b3f21a209519"
bool(true)
string(26) "reqeust_id_test_1530864034"
```

### Дивіться також

-   [SeasLog::setRequestID()](seaslog.setrequestid.html) - Встановлює диференційовані запити SeasLog requestід
-   Змінна %До в [Таблице переменных по умолчанию Seaslog](seaslog.configuration.html#ini.seaslog.default-template)