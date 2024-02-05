---
navigation:
  - splfileinfo.getpathinfo.md: '« SplFileInfo::getPathInfo'
  - splfileinfo.getperms.md: 'SplFileInfo::getPerms »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getPathname'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getPathname

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

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

**Пример #1 Пример использования**SplFileInfo::getPathname()\*\*\*\*

```php
<?php
$info = new SplFileInfo('/usr/bin/php');
var_dump($info->getPathname());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(12) "/usr/bin/php"
```

### Дивіться також

-   [SplFileInfo::getRealPath()](splfileinfo.getrealpath.md) \- Отримує абсолютний шлях до файлу
