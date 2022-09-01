---
navigation:
  - rarentry.gethostos.md: '« RarEntry::getHostOs'
  - rarentry.getname.md: 'RarEntry::getName »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::getMethod'
---
# RarEntry::getMethod

(PECL rar >= 0.1)

RarEntry::getMethod — Повертає метод компресії елемента

### Опис

```methodsynopsis
public RarEntry::getMethod(): int
```

**RarEntry::getMethod()** повертає число, що відповідає методу компресії, що використовувався при створенні поточного елемента архіву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер методу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **RarEntry::getMethod()****

```php
<?php

$rar_file = rar_open('example.rar') or die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Не удалось найти такую запись");

echo "Номер метода: " . $entry->getMethod();

?>
```
