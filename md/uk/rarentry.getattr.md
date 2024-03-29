---
navigation:
  - rarentry.extract.md: '« RarEntry::extract'
  - rarentry.getcrc.md: 'RarEntry::getCrc »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::getAttr'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarEntry::getAttr

(PECL rar >= 0.1)

RarEntry::getAttr — Повертає атрибути елемента архіву

### Опис

```methodsynopsis
public RarEntry::getAttr(): int
```

Повертає атрибути елемента архіву, що залежать від операційної системи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає атрибути або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** RarEntry::getAttr()\*\*\*\*

```php
<?php

$rar_file = rar_open('example.rar') or die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'dir/in/the/archive') or die("Не удалось найти такую запись");

$host_os = $entry->getHostOs();
$attr = $entry->getAttr();

switch($host_os) {
    case RAR_HOST_MSDOS:
    case RAR_HOST_OS2:
    case RAR_HOST_WIN32:
    case RAR_HOST_MACOS:
        printf("%c%c%c%c%c%c\n",
                ($attr & 0x08) ? 'V' : '.',
                ($attr & 0x10) ? 'D' : '.',
                ($attr & 0x01) ? 'R' : '.',
                ($attr & 0x02) ? 'H' : '.',
                ($attr & 0x04) ? 'S' : '.',
                ($attr & 0x20) ? 'A' : '.');
        break;
    case RAR_HOST_UNIX:
    case RAR_HOST_BEOS:
        switch ($attr & 0xF000)
        {
            case 0x4000:
                printf("d");
                break;
            case 0xA000:
                printf("l");
                break;
            default:
                printf("-");
                break;
        }
        printf("%c%c%c%c%c%c%c%c%c\n",
                ($attr & 0x0100) ? 'r' : '-',
                ($attr & 0x0080) ? 'w' : '-',
                ($attr & 0x0040) ? (($attr & 0x0800) ? 's':'x'):(($attr & 0x0800) ? 'S':'-'),
                ($attr & 0x0020) ? 'r' : '-',
                ($attr & 0x0010) ? 'w' : '-',
                ($attr & 0x0008) ? (($attr & 0x0400) ? 's':'x'):(($attr & 0x0400) ? 'S':'-'),
                ($attr & 0x0004) ? 'r' : '-',
                ($attr & 0x0002) ? 'w' : '-',
                ($attr & 0x0001) ? 'x' : '-');
        break;
}

rar_close($rar_file);

?>
```

### Дивіться також

-   [RarEntry::getHostOs()](rarentry.gethostos.md) \- Повертає оригінальну ОС елемента
-   Константи [RarEntry](class.rarentry.md)
