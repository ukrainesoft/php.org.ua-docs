---
navigation:
  - rarentry.getfiletime.md: '« RarEntry::getFileTime'
  - rarentry.getmethod.md: 'RarEntry::getMethod »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::getHostOs'
---
# RarEntry::getHostOs

(PECL rar >= 0.1)

RarEntry::getHostOs — Повертає оригінальну ОС елемента

### Опис

```methodsynopsis
public RarEntry::getHostOs(): int
```

Повертає код оригінальної операційної системи, у якій було створено елемент архіву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код ОС, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **RarEntry::getHostOs()**(версії >= 2.0.0)**

```php
<?php

$rar_file = rar_open('example.rar') or die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Не удалось найти такую запись");

switch ($entry->getHostOs()) {
    case RarEntry::HOST_MSDOS:
        echo "MS-DOS\n";
        break;
    case RarEntry::HOST_OS2:
        echo "OS2\n";
        break;
    case RarEntry::HOST_WIN32:
        echo "Win32\n";
        break;
    case RarEntry::HOST_MACOS:
        echo "MacOS\n";
        break;
    case RarEntry::HOST_UNIX:
        echo "Unix/Linux\n";
        break;
    case RarEntry::HOST_BEOS:
        echo "BeOS\n";
        break;
}

?>
```

**Приклад #2 **Приклад використання RarEntry::getHostOs()**(версії <= 1.0.0)**

```php
<?php

$rar_file = rar_open('example.rar') or die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Не удалось найти такую запись");

switch ($entry->getHostOs()) {
    case RAR_HOST_MSDOS:
        echo "MS-DOS\n";
        break;
    case RAR_HOST_OS2:
        echo "OS2\n";
        break;
    case RAR_HOST_WIN32:
        echo "Win32\n";
        break;
    case RAR_HOST_MACOS:
        echo "MacOS\n";
        break;
    case RAR_HOST_UNIX:
        echo "Unix/Linux\n";
        break;
    case RAR_HOST_BEOS:
        echo "BeOS\n";
        break;
}

?>
```

### Дивіться також

-   [RarEntry::extract()](rarentry.extract.md) - Витягує елемент із архіву
