---
navigation:
  - splfileinfo.getowner.md: '« SplFileInfo::getOwner'
  - splfileinfo.getpathinfo.md: 'SplFileInfo::getPathInfo »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getPath'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getPath

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getPath — Отримує шлях без імені файлу

### Опис

```methodsynopsis
public SplFileInfo::getPath(): string
```

Повертає шлях до файлу, за винятком імені файлу та завершального слішу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу.

### Приклади

**Пример #1 Пример использования**SplFileInfo::getPath()\*\*\*\*

```php
<?php
$info = new SplFileInfo('/usr/bin/php');
var_dump($info->getPath());


$info = new SplFileInfo('/usr/');
var_dump($info->getPath());?>
```

Висновок наведеного прикладу буде схожим на:

```
string(8) "/usr/bin"
string(4) "/usr"
```

### Дивіться також

-   [SplFileInfo::getRealPath()](splfileinfo.getrealpath.md) \- Отримує абсолютний шлях до файлу
-   [SplFileInfo::getFilename()](splfileinfo.getfilename.md) \- Отримує ім'я файлу
-   [SplFileInfo::getPathInfo()](splfileinfo.getpathinfo.md) \- Отримує об'єкт SplFileInfo для заданого шляху
