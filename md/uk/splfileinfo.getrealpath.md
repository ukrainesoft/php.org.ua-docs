Отримує абсолютний шлях до файлу

-   [« SplFileInfo::getPerms](splfileinfo.getperms.html)
    
-   [SplFileInfo::getSize »](splfileinfo.getsize.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує абсолютний шлях до файлу
    

# SplFileInfo::getRealPath

(PHP 5> = 5.2.2, PHP 7, PHP 8)

SplFileInfo::getRealPath — Отримує абсолютний шлях до файлу

### Опис

```methodsynopsis
public SplFileInfo::getRealPath(): string|false
```

Цей метод розпаковує всі символічні посилання, дозволяє відносні шляхи та повертає абсолютний шлях до файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу або **`false`**якщо файл не існує.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getRealPath()****

```php
<?php
$info = new SplFileInfo('/..//./../../'.__FILE__);
var_dump($info->getRealPath());

$info = new SplFileInfo('/tmp');
var_dump($info->getRealPath());

$info = new SplFileInfo('/I/Do/Not/Exist');
var_dump($info->getRealPath());

$info = new SplFileInfo('php://output');
var_dump($info->getRealPath());

$info = new SplFileInfo("");
var_dump($info->getRealPath());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(28) "/private/tmp/phptempfile.php"
string(12) "/private/tmp"
bool(false)
bool(false)
string(12) "/private/tmp"
```

### Дивіться також

-   [SplFileInfo::isLink()](splfileinfo.islink.html) - Вказує, чи є файл посиланням
-   [realpath()](function.realpath.html) - Повертає абсолютний канонізований шлях до файлу