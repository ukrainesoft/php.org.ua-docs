---
navigation:
  - function.dl.md: « dl
  - function.gc-collect-cycles.html: гкcollectcycles »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: extensionloaded
---
# extensionloaded

(PHP 4, PHP 5, PHP 7, PHP 8)

extensionloaded — Визначає, чи завантажено модуль

### Опис

```methodsynopsis
extension_loaded(string $extension): bool
```

Визначає, чи вказаний модуль завантажено.

### Список параметрів

`extension`

Ім'я модуль. Цей параметр реєстронезалежний.

Щоб переглянути всі імена модулів, скористайтеся функцією [phpinfo()](function.phpinfo.md). Якщо ви працюєте з `CGI` або `CLI`версією PHP, використовуйте параметр **м** для відображення списку доступних модулів:

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

Повертає **`true`**, якщо модуль із заданим ім'ям `extension` завантажений або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **extensionloaded()****

```php
<?php
if (!extension_loaded('gd')) {
    if (!dl('gd.so')) {
        exit;
    }
}
?>
```

### Дивіться також

-   [getloadedextensions()](function.get-loaded-extensions.html) - Повертає масив імен усіх скомпілованих та завантажених модулів
-   [getextensionfuncs()](function.get-extension-funcs.html) - Повертає масив імен функцій модуля
-   [phpinfo()](function.phpinfo.md) - Виводить інформацію про поточну конфігурацію PHP
-   [dl()](function.dl.md) - Завантажує модуль PHP під час виконання
-   [functionexists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена
