---
navigation:
  - rarentry.getunpackedsize.md: '« RarEntry::getUnpackedSize'
  - rarentry.isdirectory.md: 'RarEntry::isDirectory »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::getVersion'
---
# RarEntry::getVersion

(PECL rar >= 0.1)

RarEntry::getVersion — Повертає мінімальну версію програми RAR, необхідну для розпакування елемента

### Опис

```methodsynopsis
public RarEntry::getVersion(): int
```

Повертає мінімальну версію програми RAR (тобто WinRAR), необхідну розпакування елемента архіву. Вона закодована у вигляді: 10 основна версія + мінорна версія.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає версію або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **RarEntry::getVersion()****

```php
<?php

$rar_file = rar_open('example.rar') or die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Не удалось найти такую запись");

echo "Версия Rar, необходимая для распаковки: " . $entry->getVersion();

?>
```
