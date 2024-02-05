---
navigation:
  - seaslog.setlogger.md: '« SeasLog::setLogger'
  - seaslog.setrequestvariable.md: 'SeasLog::setRequestVariable »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::setRequestID'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::setRequestID

(PECL seaslog >=1.0.0)

SeasLog::setRequestID — Встановлює диференційовані запити SeasLog request\_id

### Опис

```methodsynopsis
public static SeasLog::setRequestID(string $request_id): bool
```

Щоб відрізнити один запит, наприклад, не викликати функції **SeasLog::setRequestId()**, при ініціалізації запиту використовується унікальне значення, що генерується вбудованою функцією \`static char\*get\_uniqid()\`

### Список параметрів

`request_id`

Рядок.

### Значення, що повертаються

Повертає TRUE у разі успішного встановлення request\_id, FALSE у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**SeasLog::setRequestID()\*\*\*\*

```php
<?php

var_dump(SeasLog::setRequestID(time() . rand()));

?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
```

### Дивіться також

-   [SeasLog::getRequestID()](seaslog.getrequestid.md) \- Отримує диференційовані запити SeasLog request\_id
