---
navigation:
  - splfileinfo.getfilename.md: '« SplFileInfo::getFilename'
  - splfileinfo.getinode.md: 'SplFileInfo::getInode »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getGroup'
---
# SplFileInfo::getGroup

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getGroup — Отримує групу файлу

### Опис

```methodsynopsis
public SplFileInfo::getGroup(): int|false
```

Отримує групу файлів. Ідентифікатор групи повертається у числовому форматі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ідентифікатор групи у числовому форматі у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає [RuntimeException](class.runtimeexception.md) у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getGroup()****

```php
<?php
$info = new SplFileInfo(__FILE__);
print_r(posix_getgrgid($info->getGroup()));
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [posixgetgrgid()](function.posix-getgrgid.md) - Повертає інформацію про групу за її ID
