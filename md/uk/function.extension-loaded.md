Визначає, чи завантажено модуль

-   [« dl](function.dl.html)
    
-   [gc\_collect\_cycles »](function.gc-collect-cycles.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Визначає, чи завантажено модуль
    

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

Щоб переглянути всі імена модулів, скористайтеся функцією [phpinfo()](function.phpinfo.html). Якщо ви працюєте з `CGI` або `CLI`версією PHP, використовуйте параметр **м** для відображення списку доступних модулів:

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

-   [get\_loaded\_extensions()](function.get-loaded-extensions.html) - Повертає масив імен усіх скомпілованих та завантажених модулів
-   [get\_extension\_funcs()](function.get-extension-funcs.html) - Повертає масив імен функцій модуля
-   [phpinfo()](function.phpinfo.html) - Виводить інформацію про поточну конфігурацію PHP
-   [dl()](function.dl.html) - Завантажує модуль PHP під час виконання
-   [function\_exists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена