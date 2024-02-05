---
navigation:
  - seaslog.getbasepath.md: '« SeasLog::getBasePath'
  - seaslog.getbufferenabled.md: 'SeasLog::getBufferEnabled »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getBuffer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::getBuffer

(PECL seaslog >=1.0.0)

SeasLog::getBuffer — Отримує буфер логів у пам'яті у вигляді масиву

### Опис

```methodsynopsis
public static SeasLog::getBuffer(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив із буфера логів у пам'яті.

### Приклади

**Приклад #1 Приклад використання** SeasLog::getBuffer()\*\*\*\*

```php
<?php

var_dump(SeasLog::info('info log'));
var_dump(SeasLog::debug('debug log'));
var_dump(SeasLog::getBuffer());

?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
array(1) {
  ["/var/log/www/default/20180707.log"]=>
  array(2) {
    [0]=>
    string(79) "2018-07-07 10:43:32 | INFO | 71785 | 5b4028d4c58d5 | 1530931412.810 | info log
"
    [1]=>
    string(81) "2018-07-07 10:43:32 | DEBUG | 71785 | 5b4028d4c58d5 | 1530931412.810 | debug log
"
  }
}
```

### Дивіться також

-   [seaslog.use\_buffer](seaslog.configuration.md#ini.seaslog.use-buffer)
-   [seaslog.buffer\_size](seaslog.configuration.md#ini.seaslog.buffer-size)
-   [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli)
-   [SeasLog::getBufferEnabled()](seaslog.getbufferenabled.md) \- Визначає, чи включено буфер
-   [SeasLog::flushBuffer()](seaslog.flushbuffer.md) \- Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp
