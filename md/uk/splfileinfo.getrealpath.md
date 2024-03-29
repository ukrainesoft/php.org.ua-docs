---
navigation:
  - splfileinfo.getperms.md: '« SplFileInfo::getPerms'
  - splfileinfo.getsize.md: 'SplFileInfo::getSize »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getRealPath'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getRealPath

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

SplFileInfo::getRealPath — Отримує абсолютний шлях до файлу

### Опис

```methodsynopsis
public SplFileInfo::getRealPath(): string|false
```

Цей метод розпаковує всі символічні посилання, дозволяє відносні шляхи та повертає абсолютний шлях до файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу або \*\*`false`\*\*якщо файл не існує.

### Приклади

**Приклад #1 Приклад використання** SplFileInfo::getRealPath()\*\*\*\*

```php
<?php
$info = new SplFileInfo('/..//./../../'.__FILE__);
var_dump($info->getRealPath());

$info = new SplFileInfo('/tmp');
var_dump($info->getRealPath());

$info = new SplFileInfo('/I/Do/Not/Exist');
var_dump($info->getRealPath());

$info = new SplFileInfo('php://output');
var_dump($info->getRealPath());

$info = new SplFileInfo("");
var_dump($info->getRealPath());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(28) "/private/tmp/phptempfile.php"
string(12) "/private/tmp"
bool(false)
bool(false)
string(12) "/private/tmp"
```

### Дивіться також

-   [SplFileInfo::isLink()](splfileinfo.islink.md) \- Вказує, чи є файл посиланням
-   [realpath()](function.realpath.md) \- Повертає абсолютний канонізований шлях до файлу
