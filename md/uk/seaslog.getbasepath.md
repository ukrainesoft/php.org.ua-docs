Отримує базовий шлях SeasLog

-   [« SeasLog::flushBuffer](seaslog.flushbuffer.html)
    
-   [SeasLog::getBuffer »](seaslog.getbuffer.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Отримує базовий шлях SeasLog
    

# SeasLog::getBasePath

(PECL seaslog >=1.0.0)

SeasLog::getBasePath — Отримує базовий шлях SeasLog

### Опис

```methodsynopsis
public static Seaslog::getBasePath(): string
```

Використовуйте функцію **SeasLog::getBasePath()**, щоб отримати значення [seaslog.default\_basepath](seaslog.configuration.html#ini.seaslog.default-basepath), яка налаштована в php.ini (seaslog.ini).

Якщо ви використовуєте [Seaslog::setBasePath()](seaslog.setbasepath.html)результат зміниться.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає значення [seaslog.default\_basepath](seaslog.configuration.html#ini.seaslog.default-basepath) у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **SeasLog::getBasePath()****

```php
<?php

var_dump(SeasLog::getBasePath());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(12) "/var/log/www"
```