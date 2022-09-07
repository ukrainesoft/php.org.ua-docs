---
navigation:
  - seaslog.setbasepath.md: '« SeasLog::setBasePath'
  - seaslog.setlogger.md: 'SeasLog::setLogger »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::setDatetimeFormat'
---
# SeasLog::setDatetimeFormat

(PECL seaslog >=1.0.0)

SeasLog::setDatetimeFormat — Встановлює стиль формату дати та часу SeasLog

### Опис

```methodsynopsis
public static SeasLog::setDatetimeFormat(string $format): bool
```

Встановлює стиль формату дати та часу SeasLog.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`format`

Рядок. Наприклад, "Y-m-d H:i:s" або "Ymd His". Дивіться перший параметр "формат" функції [date()](function.date.md)

### Значення, що повертаються

Повертає TRUE у разі успішного виконання заданого формату дати та часу, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::setDatetimeFormat()****

```php
<?php

var_dump(SeasLog::setDateTimeFormat('Ymd His'));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
```

### Дивіться також

-   [SeasLog::getDateTimeFormat()](seaslog.getdatetimeformat.md) - Отримує стиль формату дати та часу SeasLog
