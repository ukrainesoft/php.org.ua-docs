---
navigation:
  - splfileinfo.getfilename.md: '« SplFileInfo::getFilename'
  - splfileinfo.getinode.md: 'SplFileInfo::getInode »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getGroup'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getGroup

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getGroup — Отримує групу файлу

### Опис

```methodsynopsis
public SplFileInfo::getGroup(): int|false
```

Отримує групу файлів. Ідентифікатор групи повертається у числовому форматі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ідентифікатор групи у числовому форматі у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає [RuntimeException](class.runtimeexception.md)в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SplFileInfo::getGroup()\*\*\*\*

```php
<?php
$info = new SplFileInfo('example.jpg');
echo info->getFilename() . ' принадлежит группе ' . $info->getGroup() . "\n";
print_r(posix_getgrgid($info->getGroup()));
?>
```

Висновок наведеного прикладу буде схожим на:

```
example.jpg принадлежит группе 42
Array
(
    [name] => toons
    [passwd] => x
    [members] => Array
        (
            [0] => tom
            [1] => jerry
        )
    [gid] => 42
)
```

### Дивіться також

-   [filegroup()](function.filegroup.md) \- Отримує ідентифікатор групи файлу
-   [posix\_getgrgid()](function.posix-getgrgid.md) \- Повертає інформацію про групу за її ID
