Отримує список дозволів

-   [« SplFileInfo::getPathname](splfileinfo.getpathname.md)
    
-   [SplFileInfo::getRealPath »](splfileinfo.getrealpath.md)
    
-   [PHP Manual](index.md)
    
-   [SplFileInfo](class.splfileinfo.md)
    
-   Отримує список дозволів
    

# SplFileInfo::getPerms

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getPerms — Отримує список дозволів

### Опис

```methodsynopsis
public SplFileInfo::getPerms(): int|false
```

Отримує список дозволів файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає список дозволів для файлу у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getPerms()****

```php
<?php
$info = new SplFileInfo('/tmp');
echo substr(sprintf('%o', $info->getPerms()), -4);

$info = new SplFileInfo(__FILE__);
echo substr(sprintf('%o', $info->getPerms()), -4);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
1777
0644
```