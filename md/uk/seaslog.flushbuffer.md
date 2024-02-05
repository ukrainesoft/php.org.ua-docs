---
navigation:
  - seaslog.error.md: '« SeasLog::error'
  - seaslog.getbasepath.md: 'SeasLog::getBasePath »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::flushBuffer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::flushBuffer

(PECL seaslog >=1.0.0)

SeasLog::flushBuffer — Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp

### Опис

```methodsynopsis
public static SeasLog::flushBuffer(): bool
```

Очищує буфер логів за допомогою [seaslog.appender](seaslog.configuration.md#ini.seaslog.appender): робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp.

> **Зауваження** :
> 
> Смотрите также:[seaslog.appender\_retry](seaslog.configuration.md#ini.seaslog.appender-retry) [seaslog.remote\_host](seaslog.configuration.md#ini.seaslog.remote-host) [seaslog.remote\_port](seaslog.configuration.md#ini.seaslog.remote-port)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає TRUE у разі успішного очищення буфера, FALSE у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**SeasLog::flushBuffer()\*\*\*\*

```php
<?php

SeasLog::info('info log');
SeasLog::debug('debug log');
var_dump(SeasLog::getBuffer());
var_dump(SeasLog::flushBuffer());
var_dump(SeasLog::getBuffer());

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [seaslog.use\_buffer](seaslog.configuration.md#ini.seaslog.use-buffer)
-   [seaslog.buffer\_size](seaslog.configuration.md#ini.seaslog.buffer-size)
-   [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli)
-   [SeasLog::getBufferEnabled()](seaslog.getbufferenabled.md) \- Визначає, чи включено буфер
-   [SeasLog::getBuffer()](seaslog.getbuffer.md) \- Отримує буфер логів у пам'яті у вигляді масиву
