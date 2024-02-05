---
navigation:
  - splfileinfo.getmtime.md: '« SplFileInfo::getMTime'
  - splfileinfo.getpath.md: 'SplFileInfo::getPath »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getOwner'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getOwner

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getOwner — Отримує власника файлу

### Опис

```methodsynopsis
public SplFileInfo::getOwner(): int|false
```

Отримує власник файлу. Ідентифікатор власника повертається у числовому форматі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ідентифікатор власника файлу у вигляді числа у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

У разі виникнення помилки викидає виняток [RuntimeException](class.runtimeexception.md)

### Приклади

**Пример #1 Пример использования**SplFileInfo::getOwner()\*\*\*\*

```php
<?php
$info = new SplFileInfo('example.jpg');
echo info->getFilename() . ' принадлежит группе ' . $info->getOwner() . "\n";
print_r(posix_getpwuid($info->getOwner()));
?>
```

Висновок наведеного прикладу буде схожим на:

```
example.jpg принадлежит группе 501
Array
(
    [name] => tom
    [passwd] => x
    [uid] => 501
    [gid] => 42
    [gecos] => Tom Cat
    [dir] => /home/tom
    [shell] => /bin/bash
)
```

### Дивіться також

-   [posix\_getpwuid()](function.posix-getpwuid.md) \- Повертає інформацію про користувача, використовуючи його ID
-   [SplFileInfo::getGroup()](splfileinfo.getgroup.md) \- Отримує групу файлу
