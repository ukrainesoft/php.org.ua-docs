Створити новий об'єкт SplFileInfo

-   [« SplFileInfo](class.splfileinfo.html)
    
-   [SplFileInfo::getATime »](splfileinfo.getatime.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Створити новий об'єкт SplFileInfo
    

# SplFileInfo::construct

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::construct — Створити новий об'єкт SplFileInfo

### Опис

public **SplFileInfo::construct**(string `$filename`

Створює новий об'єкт SplFileInfo для вказаного імені файлу. Файл не обов'язково має існувати чи бути доступним для читання.

### Список параметрів

`filename`

Шлях до файлу.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::construct()****

```php
<?php
$info = new SplFileInfo('example.php');
if ($info->isFile()) {
    echo $info->getRealPath();
}
?>
```