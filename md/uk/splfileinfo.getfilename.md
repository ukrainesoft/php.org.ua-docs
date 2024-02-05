---
navigation:
  - splfileinfo.getfileinfo.md: '« SplFileInfo::getFileInfo'
  - splfileinfo.getgroup.md: 'SplFileInfo::getGroup »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getFilename'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getFilename

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getFilename — Отримує ім'я файлу

### Опис

```methodsynopsis
public SplFileInfo::getFilename(): string
```

Отримує ім'я файлу без інформації про шлях до нього.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я файлу.

### Приклади

**Пример #1 Пример использования**SplFileInfo::getFilename()\*\*\*\*

```php
<?php
$info = new SplFileInfo('foo.txt');
var_dump($info->getFilename());

$info = new SplFileInfo('/path/to/foo.txt');
var_dump($info->getFilename());

$info = new SplFileInfo('http://www.php.net/');
var_dump($info->getFilename());

$info = new SplFileInfo('http://www.php.net/svn.php');
var_dump($info->getFilename());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(7) "foo.txt"
string(7) "foo.txt"
string(0) ""
string(7) "svn.php"
```

### Дивіться також

-   [SplFileInfo::getBasename()](splfileinfo.getbasename.md) \- Отримує базове ім'я файлу
