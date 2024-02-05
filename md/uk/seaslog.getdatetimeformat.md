---
navigation:
  - seaslog.getbufferenabled.md: '« SeasLog::getBufferEnabled'
  - seaslog.getlastlogger.md: 'SeasLog::getLastLogger »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getDatetimeFormat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::getDatetimeFormat

(PECL seaslog >=1.0.0)

SeasLog::getDatetimeFormat — Отримує стиль формату дати та часу SeasLog

### Опис

```methodsynopsis
public static SeasLog::getDatetimeFormat(): string
```

Отримує стиль формату дати та часу SeasLog. Використовуйте функцію **SeasLog::getDatetimeFormat()**, щоб отримати значення [seaslog.default\_datetime\_format](seaslog.configuration.md#ini.seaslog.default-datetime-format), яка налаштована в php.ini(seaslog.ini).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Отримує стиль формату дати та часу SeasLog [seaslog.default\_datetime\_format](seaslog.configuration.md#ini.seaslog.default-datetime-format)Использование функции[SeasLog::setDatetimeFormat()](seaslog.setdatetimeformat.md) змінить це значення.

### Приклади

**Пример #1 Пример использования**SeasLog::getDatetimeFormat()\*\*\*\*

```php
<?php

var_dump(SeasLog::getDateTimeFormat());
var_dump(SeasLog::setDateTimeFormat('Ymd His'));
var_dump(SeasLog::getDateTimeFormat());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "Y-m-d H:i:s"
bool(true)
string(7) "Ymd His"
```

### Дивіться також

-   [SeasLog::setDatetimeFormat()](seaslog.setdatetimeformat.md) \- Встановлює стиль формату дати та часу SeasLog
