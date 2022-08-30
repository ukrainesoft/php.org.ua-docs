Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp

-   [« SeasLog::error](seaslog.error.html)
    
-   [SeasLog::getBasePath »](seaslog.getbasepath.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp
    

# SeasLog::flushBuffer

(PECL seaslog >=1.0.0)

SeasLog::flushBuffer — Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp

### Опис

```methodsynopsis
public static SeasLog::flushBuffer(): bool
```

Очищує буфер логів за допомогою [seaslog.appender](seaslog.configuration.html#ini.seaslog.appender): робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp.

> **Зауваження**
> 
> Дивіться також: [seaslog.appenderretry](seaslog.configuration.html#ini.seaslog.appender-retry) [seaslog.remotehost](seaslog.configuration.html#ini.seaslog.remote-host) [seaslog.remoteport](seaslog.configuration.html#ini.seaslog.remote-port)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає TRUE у разі успішного очищення буфера, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::flushBuffer()****

```php
<?php

SeasLog::info('info log');
SeasLog::debug('debug log');
var_dump(SeasLog::getBuffer());
var_dump(SeasLog::flushBuffer());
var_dump(SeasLog::getBuffer());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  ["/var/log/www/default/20180707.log"]=>
  array(2) {
    [0]=>
    string(79) "2018-07-07 10:47:58 | INFO | 71910 | 5b4029ded6009 | 1530931678.877 | info log
"
    [1]=>
    string(81) "2018-07-07 10:47:58 | DEBUG | 71910 | 5b4029ded6009 | 1530931678.877 | debug log
"
  }
}
bool(true)
array(0) {
}
```

### Дивіться також

-   [seaslog.usebuffer](seaslog.configuration.html#ini.seaslog.use-buffer)
-   [seaslog.buffersize](seaslog.configuration.html#ini.seaslog.buffer-size)
-   [seaslog.bufferdisabledінcli](seaslog.configuration.html#ini.seaslog.buffer-disabled-in-cli)
-   [SeasLog::getBufferEnabled()](seaslog.getbufferenabled.html) - Визначає, чи включено буфер
-   [SeasLog::getBuffer()](seaslog.getbuffer.html) - Отримує буфер логів у пам'яті у вигляді масиву