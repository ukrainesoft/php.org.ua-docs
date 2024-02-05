---
navigation:
  - splfileinfo.getpath.md: '« SplFileInfo::getPath'
  - splfileinfo.getpathname.md: 'SplFileInfo::getPathname »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getPathInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getPathInfo

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getPathInfo — Отримує об'єкт SplFileInfo для заданого шляху

### Опис

```methodsynopsis
public SplFileInfo::getPathInfo(?string $class = null): ?SplFileInfo
```

Отримує об'єкт класу [SplFileInfo](class.splfileinfo.md) для шляху поточного файлу.

### Список параметрів

`class`

Ім'я похідного від [SplFileInfo](class.splfileinfo.md) класу для використання або себе, якщо **`null`**

### Значення, що повертаються

Повертає об'єкт класу [SplFileInfo](class.splfileinfo.md) для батьківського шляху файлу у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `class` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** SplFileInfo::getPathInfo()\*\*\*\*

```php
<?php
$info = new SplFileInfo('/usr/bin/php');
$parent_info = $info->getPathInfo();
var_dump($parent_info->getRealPath());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(8) "/usr/bin"
```

### Дивіться також

-   [SplFileInfo::setInfoClass()](splfileinfo.setinfoclass.md) \- Вказує ім'я класу, об'єкти якого будуть створюватися методами SplFileInfo::getFileInfo та SplFileInfo::getPathInfo
