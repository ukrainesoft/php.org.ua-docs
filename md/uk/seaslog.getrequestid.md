---
navigation:
  - seaslog.getlastlogger.md: '« SeasLog::getLastLogger'
  - seaslog.getrequestvariable.md: 'SeasLog::getRequestVariable »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getRequestID'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::getRequestID

(PECL seaslog >=1.0.0)

SeasLog::getRequestID — Отримує диференційовані запити SeasLog request\_id

### Опис

```methodsynopsis
public static SeasLog::getRequestID(): string
```

Щоб відрізнити один запит, наприклад, не викликати функції [SeasLog::setRequestId()](seaslog.setrequestid.md), при ініціалізації запиту використовується унікальне значення, що генерується вбудованою функцією \`static char\*get\_uniqid()\`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, створений вбудованою функцією \`static char\*get\_uniqid()\` або задану функцією [SeasLog::setRequestId()](seaslog.setrequestid.md)

### Приклади

**Пример #1 Пример использования**SeasLog::getRequestID()\*\*\*\*

```php
<?php

var_dump(SeasLog::getRequestID());
var_dump(SeasLog::setRequestID('reqeust_id_test_'.time()));
var_dump(SeasLog::getRequestID());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(13) "5b3f21a209519"
bool(true)
string(26) "reqeust_id_test_1530864034"
```

### Дивіться також

-   [SeasLog::setRequestID()](seaslog.setrequestid.md) \- Встановлює диференційовані запити SeasLog request\_id
-   Переменная\`%Q\`в[Таблиці змінних за промовчанням Seaslog](seaslog.configuration.md#ini.seaslog.default-template)
