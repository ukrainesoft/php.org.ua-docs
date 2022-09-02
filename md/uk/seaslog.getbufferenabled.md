---
navigation:
  - seaslog.getbuffer.md: '« SeasLog::getBuffer'
  - seaslog.getdatetimeformat.md: 'SeasLog::getDatetimeFormat »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getBufferEnabled'
---
# SeasLog::getBufferEnabled

(PECL seaslog >=1.0.0)

SeasLog::getBufferEnabled — Визначає, чи буфер увімкнено.

### Опис

```methodsynopsis
public static SeasLog::getBufferEnabled(): bool
```

Результат об'єднання [seaslog.usebuffer](seaslog.configuration.md#ini.seaslog.use-buffer) і [seaslog.bufferdisabledінcli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає TRUE, якщо [seaslog.usebuffer](seaslog.configuration.md#ini.seaslog.use-buffer) є true. Якщо увімкнути [seaslog.bufferdisabledінcli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli) та запустити в cli, параметр seaslog.usebuffer буде скинутий, Seaslog НЕГАЙНО перезапише дані в сховище даних.

### Приклади

**Приклад #1 Приклад використання **SeasLog::getBufferEnabled()****

```php
<?php

var_dump(SeasLog::getBufferEnabled());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
```

### Дивіться також

-   [seaslog.usebuffer](seaslog.configuration.md#ini.seaslog.use-buffer)
-   [seaslog.buffersize](seaslog.configuration.md#ini.seaslog.buffer-size)
-   [seaslog.bufferdisabledінcli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli)
-   [SeasLog::getBuffer()](seaslog.getbuffer.md) - Отримує буфер логів у пам'яті у вигляді масиву
-   [SeasLog::flushBuffer()](seaslog.flushbuffer.md) - Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp
