Отримує об'єкт SplFileInfo для заданого шляху

-   [« SplFileInfo::getPath](splfileinfo.getpath.html)
    
-   [SplFileInfo::getPathname »](splfileinfo.getpathname.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує об'єкт SplFileInfo для заданого шляху
    

# SplFileInfo::getPathInfo

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getPathInfo — Отримує об'єкт SplFileInfo для заданого шляху

### Опис

```methodsynopsis
public SplFileInfo::getPathInfo(?string $class = null): ?SplFileInfo
```

Отримує об'єкт класу [SplFileInfo](class.splfileinfo.html) для шляху поточного файлу

### Список параметрів

`class`

Ім'я похідного від [SplFileInfo](class.splfileinfo.html) класу для використання або себе, якщо **`null`**

### Значення, що повертаються

Повертає об'єкт класу [SplFileInfo](class.splfileinfo.html) для батьківського шляху файлу у разі успішного виконання або **`null`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `class` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getPathInfo()****

```php
<?php
$info = new SplFileInfo('/usr/bin/php');
$parent_info = $info->getPathInfo();
var_dump($parent_info->getRealPath());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(8) "/usr/bin"
```

### Дивіться також

-   [SplFileInfo::setInfoClass()](splfileinfo.setinfoclass.html) - Вказує ім'я класу, об'єкти якого будуть створюватися методами SplFileInfo::getFileInfo та SplFileInfo::getPathInfo