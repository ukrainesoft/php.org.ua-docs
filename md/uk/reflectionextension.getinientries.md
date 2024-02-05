---
navigation:
  - reflectionextension.getfunctions.md: '« ReflectionExtension::getFunctions'
  - reflectionextension.getname.md: 'ReflectionExtension::getName »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::getINIEntries'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::getINIEntries

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::getINIEntries — Отримання ini-налаштувань модуля

### Опис

```methodsynopsis
public ReflectionExtension::getINIEntries(): array
```

Отримує ini-налаштування модуля.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив array, у якому ключі - імена ini-налаштувань, а значення - відповідні значення налаштувань.

### Приклади

**Приклад #1 Приклад використання** ReflectionExtension::getINIEntries()\*\*\*\*

```php
<?php
$ext = new ReflectionExtension('mysql');

print_r($ext->getINIEntries());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [mysql.allow_persistent] => 1
    [mysql.max_persistent] => -1
    [mysql.max_links] => -1
    [mysql.default_host] =>
    [mysql.default_user] =>
    [mysql.default_password] =>
    [mysql.default_port] =>
    [mysql.default_socket] =>
    [mysql.connect_timeout] => 60
    [mysql.trace_mode] =>
    [mysql.allow_local_infile] => 1
    [mysql.cache_size] => 2000
)
```

### Дивіться також

-   [ini\_get\_all()](function.ini-get-all.md) \- Отримує всі налаштування конфігурації
-   [ReflectionExtension::getConstants()](reflectionextension.getconstants.md) \- Отримання констант
