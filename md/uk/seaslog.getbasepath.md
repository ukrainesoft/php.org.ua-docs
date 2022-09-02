---
navigation:
  - seaslog.flushbuffer.md: '« SeasLog::flushBuffer'
  - seaslog.getbuffer.md: 'SeasLog::getBuffer »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getBasePath'
---
# SeasLog::getBasePath

(PECL seaslog >=1.0.0)

SeasLog::getBasePath — Отримує базовий шлях SeasLog

### Опис

```methodsynopsis
public static Seaslog::getBasePath(): string
```

Використовуйте функцію **SeasLog::getBasePath()**, щоб отримати значення [seaslog.defaultbasepath](seaslog.configuration.md#ini.seaslog.default-basepath), яка налаштована в php.ini (seaslog.ini).

Якщо ви використовуєте [Seaslog::setBasePath()](seaslog.setbasepath.md)результат зміниться.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає значення [seaslog.defaultbasepath](seaslog.configuration.md#ini.seaslog.default-basepath) у вигляді рядка.

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
