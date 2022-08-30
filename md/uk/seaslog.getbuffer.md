Отримує буфер логів у пам'яті у вигляді масиву

-   [« SeasLog::getBasePath](seaslog.getbasepath.html)
    
-   [SeasLog::getBufferEnabled »](seaslog.getbufferenabled.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Отримує буфер логів у пам'яті у вигляді масиву
    

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

**Приклад #1 Приклад використання **SeasLog::getBuffer()****

```php
<?php

var_dump(SeasLog::info('info log'));
var_dump(SeasLog::debug('debug log'));
var_dump(SeasLog::getBuffer());

?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [seaslog.usebuffer](seaslog.configuration.html#ini.seaslog.use-buffer)
-   [seaslog.buffersize](seaslog.configuration.html#ini.seaslog.buffer-size)
-   [seaslog.bufferdisabledінcli](seaslog.configuration.html#ini.seaslog.buffer-disabled-in-cli)
-   [SeasLog::getBufferEnabled()](seaslog.getbufferenabled.html) - Визначає, чи включено буфер
-   [SeasLog::flushBuffer()](seaslog.flushbuffer.html) - Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp