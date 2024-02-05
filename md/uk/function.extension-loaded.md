---
navigation:
  - function.dl.md: « dl
  - function.gc-collect-cycles.md: gc\_collect\_cycles »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: extension\_loaded
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# extension\_loaded

(PHP 4, PHP 5, PHP 7, PHP 8)

extension\_loaded — Визначає, чи модуль завантажений.

### Опис

```methodsynopsis
extension_loaded(string $extension): bool
```

Визначає, чи вказаний модуль завантажено.

### Список параметрів

`extension`

Ім'я модуль. Цей параметр реєстронезалежний.

Щоб переглянути всі імена модулів, скористайтеся функцією [phpinfo()](function.phpinfo.md). Якщо ви працюєте з `CGI`\-или`CLI`\-версией PHP, используйте параметр**\-m** для відображення списку доступних модулів:

```
$ php -m
[PHP Modules]
xml
tokenizer
standard
sockets
session
posix
pcre
overload
mysql
mbstring
ctype

[Zend Modules]
```

### Значення, що повертаються

Повертає **`true`**, якщо модуль із заданим ім'ям `extension`загружен или\*\*`false`\*\* в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** extension\_loaded()\*\*\*\*

```php
<?php
if (!extension_loaded('gd')) {
    if (!dl('gd.so')) {
        exit;
    }
}
?>
```

### Дивіться також

-   [get\_loaded\_extensions()](function.get-loaded-extensions.md) \- Повертає масив імен усіх скомпілованих та завантажених модулів
-   [get\_extension\_funcs()](function.get-extension-funcs.md) \- Повертає масив імен функцій модуля
-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
-   [dl()](function.dl.md) \- Завантажує модуль PHP під час виконання
-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
