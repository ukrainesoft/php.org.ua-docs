Визначає, чи включено буфер

-   [« SeasLog::getBuffer](seaslog.getbuffer.html)
    
-   [SeasLog::getDatetimeFormat »](seaslog.getdatetimeformat.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Визначає, чи включено буфер
    

# SeasLog::getBufferEnabled

(PECL seaslog >=1.0.0)

SeasLog::getBufferEnabled — Визначає, чи буфер увімкнено.

### Опис

```methodsynopsis
public static SeasLog::getBufferEnabled(): bool
```

Результат об'єднання [seaslog.use\_buffer](seaslog.configuration.html#ini.seaslog.use-buffer) і [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.html#ini.seaslog.buffer-disabled-in-cli)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає TRUE, якщо [seaslog.use\_buffer](seaslog.configuration.html#ini.seaslog.use-buffer) є true. Якщо увімкнути [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.html#ini.seaslog.buffer-disabled-in-cli) та запустити в cli, параметр seaslog.usebuffer буде скинутий, Seaslog НЕГАЙНО перезапише дані в сховище даних.

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

-   [seaslog.use\_buffer](seaslog.configuration.html#ini.seaslog.use-buffer)
-   [seaslog.buffer\_size](seaslog.configuration.html#ini.seaslog.buffer-size)
-   [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.html#ini.seaslog.buffer-disabled-in-cli)
-   [SeasLog::getBuffer()](seaslog.getbuffer.html) - Отримує буфер логів у пам'яті у вигляді масиву
-   [SeasLog::flushBuffer()](seaslog.flushbuffer.html) - Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp