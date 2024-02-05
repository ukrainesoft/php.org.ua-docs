---
navigation:
  - reflectionextension.getversion.md: '« ReflectionExtension::getVersion'
  - reflectionextension.ispersistent.md: 'ReflectionExtension::isPersistent »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::info'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::info

(PHP 5 >= 5.2.4, PHP 7, PHP 8)

ReflectionExtension::info — Виведення інформації про модуль

### Опис

```methodsynopsis
public ReflectionExtension::info(): void
```

Виводить фрагмент "[phpinfo()](function.phpinfo.md)для зазначеного модуля.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Інформація про модуль.

### Приклади

**Пример #1 Пример использования**ReflectionExtension::info()\*\*\*\*

```php
<?php
$ext = new ReflectionExtension('mysqli');
$ext->info();
?>
```

Висновок наведеного прикладу буде схожим на:

```
mysqli

MysqlI Support => enabled
Client API library version => mysqlnd 5.0.5-dev - 081106 - $Revision$
Active Persistent Links => 0
Inactive Persistent Links => 0
Active Links => 0
Persistent cache => enabled
put_hits => 0
put_misses => 0
get_hits => 0
get_misses => 0
size => 2000
free_items => 2000
references => 2

Directive => Local Value => Master Value
mysqli.max_links => Unlimited => Unlimited
mysqli.max_persistent => Unlimited => Unlimited
mysqli.allow_persistent => On => On
mysqli.default_host => no value => no value
mysqli.default_user => no value => no value
mysqli.default_pw => no value => no value
mysqli.default_port => 3306 => 3306
mysqli.default_socket => no value => no value
mysqli.reconnect => Off => Off
mysqli.allow_local_infile => On => On
mysqli.cache_size => 2000 => 2000
```

### Дивіться також

-   [ReflectionExtension::getName()](reflectionextension.getname.md) \- Отримання імені модуля
-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
