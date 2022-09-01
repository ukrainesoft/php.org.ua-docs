---
navigation:
  - seaslog.getbufferenabled.html: '« SeasLog::getBufferEnabled'
  - seaslog.getlastlogger.html: 'SeasLog::getLastLogger »'
  - index.html: PHP Manual
  - class.seaslog.html: SeasLog
title: 'SeasLog::getDatetimeFormat'
---
# SeasLog::getDatetimeFormat

(PECL seaslog >=1.0.0)

SeasLog::getDatetimeFormat — Отримує стиль формату дати та часу SeasLog

### Опис

```methodsynopsis
public static SeasLog::getDatetimeFormat(): string
```

Отримує стиль формату дати та часу SeasLog. Використовуйте функцію **SeasLog::getDatetimeFormat()**, щоб отримати значення [seaslog.defaultdatetimeformat](seaslog.configuration.html#ini.seaslog.default-datetime-format), яка налаштована в php.ini(seaslog.ini).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Отримує стиль формату дати та часу SeasLog [seaslog.defaultdatetimeformat](seaslog.configuration.html#ini.seaslog.default-datetime-format). Використання функції [SeasLog::setDatetimeFormat()](seaslog.setdatetimeformat.html) змінить це значення.

### Приклади

**Приклад #1 Приклад використання **SeasLog::getDatetimeFormat()****

```php
<?php

var_dump(SeasLog::getDateTimeFormat());
var_dump(SeasLog::setDateTimeFormat('Ymd His'));
var_dump(SeasLog::getDateTimeFormat());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "Y-m-d H:i:s"
bool(true)
string(7) "Ymd His"
```

### Дивіться також

-   [SeasLog::setDatetimeFormat()](seaslog.setdatetimeformat.html) - Встановлює стиль формату дати та часу SeasLog
