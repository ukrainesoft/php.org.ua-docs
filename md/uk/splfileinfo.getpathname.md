Отримує шлях до файлу

-   [« SplFileInfo::getPathInfo](splfileinfo.getpathinfo.html)
    
-   [SplFileInfo::getPerms »](splfileinfo.getperms.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує шлях до файлу
    

# SplFileInfo::getPathname

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getPathname — Отримує шлях до файлу

### Опис

```methodsynopsis
public SplFileInfo::getPathname(): string
```

Повертає шлях до файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Шлях до файлу.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getPathname()****

```php
<?php
$info = new SplFileInfo('/usr/bin/php');
var_dump($info->getPathname());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(12) "/usr/bin/php"
```

### Дивіться також

-   [SplFileInfo::getRealPath()](splfileinfo.getrealpath.html) - Отримує абсолютний шлях до файлу