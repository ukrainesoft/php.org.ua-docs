---
navigation:
  - seaslog.setlogger.html: '« SeasLog::setLogger'
  - seaslog.setrequestvariable.html: 'SeasLog::setRequestVariable »'
  - index.html: PHP Manual
  - class.seaslog.html: SeasLog
title: 'SeasLog::setRequestID'
---
# SeasLog::setRequestID

(PECL seaslog >=1.0.0)

SeasLog::setRequestID — Встановлює диференційовані запити SeasLog requestід

### Опис

```methodsynopsis
public static SeasLog::setRequestID(string $request_id): bool
```

Щоб відрізнити один запит, наприклад, не викликати функції **SeasLog::setRequestId()**, при ініціалізації запиту використовується унікальне значення, що генерується вбудованою функцією static char getuniqid()

### Список параметрів

`request_id`

Рядок.

### Значення, що повертаються

Повертає TRUE у разі успішного встановлення requestid, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::setRequestID()****

```php
<?php

var_dump(SeasLog::setRequestID(time() . rand()));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
```

### Дивіться також

-   [SeasLog::getRequestID()](seaslog.getrequestid.html) - Отримує диференційовані запити SeasLog requestід
