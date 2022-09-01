---
navigation:
  - splfileinfo.getmtime.md: '« SplFileInfo::getMTime'
  - splfileinfo.getpath.md: 'SplFileInfo::getPath »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getOwner'
---
# SplFileInfo::getOwner

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getOwner — Отримує власника файлу

### Опис

```methodsynopsis
public SplFileInfo::getOwner(): int|false
```

Отримує власник файлу. Ідентифікатор власника повертається у числовому форматі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ідентифікатор власника файлу у вигляді числа у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

У разі виникнення помилки викидає виняток [RuntimeException](class.runtimeexception.md)

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getOwner()****

```php
<?php
$info = new SplFileInfo('file.txt');
print_r(posix_getpwuid($info->getOwner()));
?>
```

### Дивіться також

-   [posixgetpwuid()](function.posix-getpwuid.html) - Повертає інформацію про користувача, використовуючи його ID
-   [SplFileInfo::getGroup()](splfileinfo.getgroup.md) - Отримує групу файлу
