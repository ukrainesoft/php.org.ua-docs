Отримує базове ім'я файлу

-   [« SplFileInfo::getATime](splfileinfo.getatime.html)
    
-   [SplFileInfo::getCTime »](splfileinfo.getctime.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує базове ім'я файлу
    

# SplFileInfo::getBasename

(PHP 5> = 5.2.2, PHP 7, PHP 8)

SplFileInfo::getBasename — Отримує базове ім'я файлу

### Опис

```methodsynopsis
public SplFileInfo::getBasename(string $suffix = ""): string
```

Цей метод повертає базове ім'я файлу, каталогу або посилання без інформації про шлях.

### Список параметрів

`suffix`

Необов'язковий суфікс, який виключено з базового імені.

**Застереження**

**SplFileInfo::getBasename()** враховує локаль, тому щоб побачити коректне базове ім'я файлу з багатобайтовими символами в дорозі, відповідна локаль повинна бути встановлена ​​за допомогою функції [setlocale()](function.setlocale.html)

### Значення, що повертаються

Повертає базове ім'я без інформації про шлях.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getBasename()****

```php
<?php
$info = new SplFileInfo('file.txt');
var_dump($info->getBasename());

$info = new SplFileInfo('/path/to/file.txt');
var_dump($info->getBasename());

$info = new SplFileInfo('/path/to/file.txt');
var_dump($info->getBasename('.txt'));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(8) "file.txt"
string(8) "file.txt"
string(4) "file"
```

### Дивіться також

-   [SplFileInfo::getFilename()](splfileinfo.getfilename.html) - Отримує ім'я файлу