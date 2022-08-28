Отримує розширення файлу

-   [« SplFileInfo::getCTime](splfileinfo.getctime.html)
    
-   [SplFileInfo::getFileInfo »](splfileinfo.getfileinfo.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує розширення файлу
    

# SplFileInfo::getExtension

(PHP 5> = 5.3.6, PHP 7, PHP 8)

SplFileInfo::getExtension — Отримує розширення файлу

### Опис

```methodsynopsis
public SplFileInfo::getExtension(): string
```

Повертає розширення файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що містить розширення файлу, або порожній рядок (string), якщо файл не має розширення.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getExtension()****

```php
<?php

$info = new SplFileInfo('foo.txt');
var_dump($info->getExtension());

$info = new SplFileInfo('photo.jpg');
var_dump($info->getExtension());

$info = new SplFileInfo('something.tar.gz');
var_dump($info->getExtension());

?>
```

Результат виконання цього прикладу:

```
string(3) "txt"
string(3) "jpg"
string(2) "gz"
```

### Примітки

> **Зауваження**
> 
> Інший спосіб отримання розширення - використання функції [pathinfo()](function.pathinfo.html)
> 
> ```php
> <?php
> $extension = pathinfo($info->getFilename(), PATHINFO_EXTENSION);
> ?>
> ```

### Дивіться також

-   [SplFileInfo::getFilename()](splfileinfo.getfilename.html) - Отримує ім'я файлу
-   [SplFileInfo::getBasename()](splfileinfo.getbasename.html) - Отримує базове ім'я файлу
-   [pathinfo()](function.pathinfo.html) - Повертає інформацію про шлях до файлу