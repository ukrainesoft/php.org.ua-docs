---
navigation:
  - seaslog.getbuffer.md: '« SeasLog::getBuffer'
  - seaslog.getdatetimeformat.md: 'SeasLog::getDatetimeFormat »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getBufferEnabled'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::getBufferEnabled

(PECL seaslog >=1.0.0)

SeasLog::getBufferEnabled — Визначає, чи увімкнено буфер.

### Опис

```methodsynopsis
public static SeasLog::getBufferEnabled(): bool
```

Результат об'єднання [seaslog.use\_buffer](seaslog.configuration.md#ini.seaslog.use-buffer) і [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає TRUE, якщо [seaslog.use\_buffer](seaslog.configuration.md#ini.seaslog.use-buffer) є true. Якщо увімкнути [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli) та запустити в cli, параметр seaslog.use\_buffer буде скинутий, Seaslog НЕГАЙНО перезапише дані в сховище даних.

### Приклади

**Пример #1 Пример использования**SeasLog::getBufferEnabled()\*\*\*\*

```php
<?php

var_dump(SeasLog::getBufferEnabled());

?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
```

### Дивіться також

-   [seaslog.use\_buffer](seaslog.configuration.md#ini.seaslog.use-buffer)
-   [seaslog.buffer\_size](seaslog.configuration.md#ini.seaslog.buffer-size)
-   [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli)
-   [SeasLog::getBuffer()](seaslog.getbuffer.md) \- Отримує буфер логів у пам'яті у вигляді масиву
-   [SeasLog::flushBuffer()](seaslog.flushbuffer.md) \- Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp
